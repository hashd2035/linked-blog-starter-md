---
icon: luc_briefcase
---
```toc
```
[[Concurrency in Java]]
[[Concurrency Design Principles and Best Practices]]
# Concurrency Exercises
https://github.com/loong/go-concurrency-exercises

# Concurrency Problems

## Problem: Message Broadcaster (Pub/Sub)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/2e61b823-1633-45fa-aaee-98ba1576b3c0/Untitled.png)

- Publisher publishes to many topics
- A topic sends messages to a subscription
- Subscriber subscribes to many subscriptions

This can be used in any kind of broadcasting scenario, for example, this kind of system can be used to in Youtube. The publisher publishes a new video in a channel (topic), subscribers gets notification that the new video is available.

### Requirements

- Needs to track subscribers to topics (subscriptions) in a multithreaded environment. This is our critical section
    - A new subscriber can be recorded
    - A subscriber can unsubscribe from a topic

### Publish-Subscribe Pattern

Publish-Subscribe is a messaging pattern where publishers categorize messages into different classes (topics) without knowledge of subscribers

- Subscribers express interest in topics and only receive message that belong to the subscribed topic
- This pattern provides increased scalability.
- It also gives loose coupling between subscribers and publishers (unlike traditional client-server paradigm)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/83616097-7190-4ca6-8457-4b8945f3098e/Untitled.png)

Note: Keep in mind that this is simplified solution.

Explanation Video: [https://uplevel.interviewkickstart.com/resource/rc-video-711274-1132248-219-9019](https://uplevel.interviewkickstart.com/resource/rc-video-711274-1132248-219-9019) @06:30

```cpp
ConcurrentHashMap // Thread-safe hashmap
Compare-and-Swap (CAS) operation 
```

### Improvements

- Enforce message delivery guarantees/retry logic around the pub-sub architecture
    - Subscriber publishes receipt messages
- Publisher assumes that subscribers are listening
    - Subscribers should indicate errors through logging/metrics
- Large message volume flow may slow down the overall system
    - Topics can be sharded

## Problem: Reader Write Lock

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/44c4da75-b870-4684-aefe-70abe478efbf/Untitled.png)

[https://java-design-patterns.com/patterns/reader-writer-lock/#applicability](https://java-design-patterns.com/patterns/reader-writer-lock/#applicability)

A readers–writer is a synchronization primitive that solves one of the readers–writers problems.

- An RW lock allows concurrent access for read-only operations, whereas write operations require exclusive access.
- This means that multiple threads can read the data in parallel but an exclusive lock is needed for writing or modifying data.
- When a writer is writing the data, all other writers and readers will be blocked until the writer is finished writing.
- A common use might be to control access to a data structure in memory that cannot be updated atomically and is invalid (and should not be read by another thread) until the update is complete.

Readers–writer locks are usually constructed on top of mutexes and condition variables, or on top of semaphores.

[44 - Implement Read Write Lock - SOLUTION - Code Demo](https://www.youtube.com/watch?v=SGtzx3jL1Uo)

### Requirements/Specification

- Cannot use a mutex alone to control when readers/writers have access to critical section
- Need two conditional variables
    - Conditional 1 (reader): A reader can only read if there are no active writers or pending write requests
    - Conditional 2 (writer): A write can only write if there are no current readers or writers (second condition can change if you want to support re-entry by the same writer)
- We will implement a simple read write lock that allows multi reader and single writer
- Writers are given precedence to prevent starvation of writer (high read requests)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/e3cda245-36b0-47d6-9553-e0de469bab24/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/cd5017e0-ce8d-4d9e-a5e4-bbf7f7be6f1e/0a47c575-e088-4e2e-ab30-8c14986889ea/Untitled.png)

## Problem: Odd-Even Problem using condition variables

[IK Odd even with condition variables, Yannis](https://www.youtube.com/embed/e0j99cDkt8U?showinfo=0)

## Problem: Sequence Generator

- DB Unique Id’s, etc.

### requirements

- Unique (Sequence is continuous and contiguous)

**interface**

```java
public interface SequenceGenerator {
    int getNext();
}
```

**unsafeSequenceGenerator**

```java
public class UnsafeSequenceGenerator implements SequenceGenerator {
    private  int sequenceNumber;
    public UnsafeSequenceGenerator() {
        this.sequenceNumber = 0;
    }
    public int getNext() { return this.sequenceNumber++; }
}
```

**synchronizedSequenceGenerator**

```java
public class SynchronizedSequenceGenerator implements SequenceGenerator {
    private int sequenceNumber;
    public SynchronizedSequenceGenerator() {
        this.sequenceNumber = 0;
    }
    public synchronized int getNext() {
        return this.sequenceNumber++;
    }
}
```

**atomicSequenceGenerator**

```java
public class AtomicSequenceGenerator implements SequenceGenerator {
    private AtomicInteger sequenceNumber;
    public AtomicSequenceGenerator() {
        this.sequenceNumber = new AtomicInteger(0);
    }
    public int getNext() {
        return this.sequenceNumber.getAndIncrement();
    }
}
```

## Problem: Thread-safe Singleton
https://www.baeldung.com/java-singleton-double-checked-locking

```java
package com.ik.backend.concurrency.design_pattern;

/**
 * Thread safe singleton with lazy initialization.
 */
public class Singleton {

    private static Singleton instance; // singleton = private and static!!

    /**
     * Private constructor.
     */
    private Singleton() {   // private constructor
    }

    /**
     * Many threads can enter this method but only one thread
     * will initialize the instance without blocking other threads.
     *
     * @return the instance
     */
    public static Singleton getInstance() {
        // First check to see if the instance has not been initialized by another thread
        if (instance == null) { 
            // Only one thread will initialize.  If not then get a lock and initialize the instance other threads will not be blocked
            System.out.println(Thread.currentThread().getName() + " got a null instance.");
            
            
            synchronized (Singleton.class) { // lock is the class itself
                System.out.println(Thread.currentThread().getName() + " obtained lock.");
                // double check pattern
                if (instance == null) {
                    System.out.println(Thread.currentThread().getName() + " will initialized instance.");
                    // if instance is null, initialize
                    instance = new Singleton();
                    System.out.println(Thread.currentThread().getName() + " initialized singleton instance " + instance.toString());
                }
            }
        }
        return instance;
    }

}

```

## Problem: Dining Philosophers

## Problem: Transactions

## Problem: Signaling



https://stackoverflow.com/questions/1970345/what-is-thread-contention