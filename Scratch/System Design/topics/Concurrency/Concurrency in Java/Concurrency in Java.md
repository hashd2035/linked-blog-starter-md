---
icon: luc_briefcase
---
```toc
```
## Java Constructs
https://www.bairesdev.com/blog/java-concurrency/
https://jenkov.com/tutorials/java-concurrency/creating-and-starting-threads.html

```vid
https://www.youtube.com/watch?v=mTGdtC9f4EU&list=PLL8woMHwr36EDxjUoCzboZjedsnhLP1j4
```

- Creating Threads
    
- Executing Threads
    
- Synchronizing Them
    
- `volitile` - Low Level construct, Not used widely these days.
https://www.baeldung.com/java-volatile
    
- ThreadPool - Used for Parallel Processing
    
- Future

### Virtual Threads
https://www.infoworld.com/article/3678148/intro-to-virtual-threads-a-new-approach-to-java-concurrency.html

```vid
https://www.youtube.com/watch?v=kirhhcFAGB4&list=PLL8woMHwr36Fzz51PjWjfMKelvOaAX9RW
```

### Atomic Variables

[An Introduction to Atomic Variables in Java | Baeldung](https://www.baeldung.com/java-atomic-variables)

`AtomicInteger`, `AtomicLong`, `AtomicBoolean`, `AtomicReference`

Thread is implemented using Runnable (return void), Callable (return value)

Executors - executes threads

### Concurrent Map
https://www.baeldung.com/java-concurrent-map