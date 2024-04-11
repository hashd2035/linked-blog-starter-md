---
icon: luc_briefcase
---

```toc
```

## Parallelism vs Concurrency

- Parallelism
    - Multiple functions executing simultaneously
        - Or, parts of a single function executing simultaneously
    - Opposite is serialism
- Concurrency
    - Functions **interleave**
    - Opposite is sequential

## When do we not need concurrency?

- No concurrency problem when reading. The problem is when writing happens with the shared resources.
- Functions with independent data
    - Processes
    - Full Task completes before next task
    - Map-Reduce, Nodejs, PHP, etc.

## When do we need concurrency **primitives**?

- Functions with dependent data
    - Threads
    - Tasks can be interrupted and their intermediate state observed
    - Java, C#, C++

## Blocked vs Running

Thread can be either running or blocked

- Blocked thread do not execute
    - prevents code from corrupting shared state
    - used by all OS primitives to achieve exclusivity
- Running threads can still synchronize with the hardware support
    - interlocked operations
    - atomic operations
- Avoid busy-waiting
    - Use primitives (not something like while loop tricks, etc)
        - Don’t try to outsmart the scheduler, it won’t work.

## OS Synchronization primitives

### 1. Critical section
: Java: Reentrant lock
: Linux: In-process Mutex

Another name could be a lock
Also, known as mutex
Has two states, taken and free

- used to enforce exclusive access between threads
- cannot be used between processes
- light-weight, relative to other primitives
    - Very efficient in one particular case that is when the lock is uncontended
    - uncontended locks do not require kernel transition
    - uncontended locks is a lock that no threads currently owns
    - Or, in other words, An uncontended lock is **a lock that a thread acquires without any competition**
        - If a lock is free and thread A comes along and asks for the lock, the lock is uncontended
        - Thread A completes its work and releases the lock. The lock is still uncontended
        - Thread B comes along and acquires the lock, the lock is uncontended
        - Now thread C comes in and try to get the lock
            - The lock becomes contended
            - There is more than one thread that is trying to interact with the lock
- Usually, more efficient than (General) Mutex (see below)

### 2. Mutex
:Java: Lock (implemented using `synchronized` keyword)
:Linux: Cross-process (Interprocess) mutex

Also, Has two states, taken and free
- Allows both thread and process synchronization
- Always results in a kernel transition
- kernel transition (asking OS kernel to take over the job. And it’s expensive)
    - In-process Mutex (Critical section) is always cheaper than Cross-process Mutex

### 3. Condition variable
:java: [Condition](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/locks/Condition.html)

- Allows both thread and process synchronization
- Associated with Mutex
- Lets us specify user defined conditions on our mutex
- Must handle spurious waking
    - a spurious wakeup **occurs when a thread wakes up from waiting on a condition variable without the variable being satisfied**.
    - To handle spurious wakeups, threads should always recheck the condition after being awakened from a wait. This can be done using a while loop, as shown in the following example → Always, Always, Always, use `while` and not `if`
        
        ```java
        while (!condition) {
          condition.wait();
        }
        ```
        
- Critical Section and Mutex do not have spurious waking.
    - But, condition variable is much faster.

### 4. Semaphore

- Allows both thread and process synchronization
- Always results in a kernel transition
- Is not really about locking. It’s about counting
    - Initialized to a count.
    - Wait decrement the count, signal increments the count
    - When waited on by thread, the count is reduced.
    - When count goes to 0, lock is taken
    - If you signal, then, the count is incremented and if there is a thread waiting, then the thread is woken up
- The grand daddy of primitives - mutex and critical section
    - Can be clunky, compared to others
    - Can do everything you ever need
    - Mutex is just a semaphore with a count of 1
    - According to instructor, it is almost never used.
- A **bounding buffer** may use a counting semaphore to limit the number of threads that can access a data structure

### 5. Interlocked Operation
:Linux: Atomic Operation

- More of hardware primitive than an operating system primitive
    - So, usually have hardware support
        - Or, otherwise, must be simulated with OS primitives
    - Much faster than OS primitives
        - No kernel transition, hardware is doing it.
- Low-level operations that appear atomic to running threads
    - Swap
    - Increment (e.g. reference counting)
    - …
- Atomic operations do not block thread
    - They complete a unit of work in a separate single thread

## Deadlock

- All threads are waiting for a lock
- No threads can make progress to release the locks they hold
    - e.g. Data dependency cycle
        - A waits for B
        - B waits for A
- Tips to avoid
    - The way not to have deadlock is not to have data dependency cycle
        - Which sounds easy in principle, but, is hard in practice
    - Do not call unknown functions from inside lock
    - Always take locks in a specific order (static ordering)
        - e.g. A take a lock, then, B takes a lock in order
        - Might be impractical in large system
    - So, for a large system, have a deadlock detector running alongside

## Race Condition

**A race condition occurs when two or more threads access the same shared resource at the same time**.

This can lead to unexpected behavior due to a lack of synchronization between the threads. For example, if two people try to deposit $1 online into the same bank account, the final amount might be $18 instead of $19 due to race conditions.

## Lazy Init

Why use lazy Initialization

What’s wrong with this code?

```cpp
Type* pFoo

getSinglton
	if (NULL = pFoo)
			pFoo = MakeFoo()
			
	return pFoo
```

### Double-Checked locking (Double-Check pattern)

[https://www.baeldung.com/java-singleton-double-checked-locking](https://www.baeldung.com/java-singleton-double-checked-locking)

```cpp
Type *pFoo // our global
CriticalSection csFoo;

getSingleton
	if (NULL == pFoo)
			csFoo.Enter // get the lock
			if (NULL == pFoo) // double check
					pFool = MakeFoo()
			csFoo.Leave
			
	return pFoo
```

