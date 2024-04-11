Compare-and-swap (CAS) is an <u>atomic instruction</u> in computer science that uses multithreading to achieve synchronization. It compares the contents of a memory location with a given value and modifies the contents to a new given value if they are the same. This is done as a single atomic operation, which ensures that the new value is calculated based on up-to-date information

CAS is a common technique in lock-free algorithms to ensure that updates to shared memory by one thread fail if another thread has modified the same space in the meantime. CAS involves three parameters: a memory location (address), an expected old value, and a new value. If the current value at the specified memory location matches the expected old value, the new value is written. Otherwise, the operation fails, and the algorithm must retry.

CAS is a powerful tool for achieving thread safety without locks because of its low-level interaction with memory and hardware instructions.

Compare and Swap in Java
```vid
https://www.youtube.com/watch?v=ufWVK7CHOAk&t=3
```
