In the context of distributed systems, monotonicity refers to the property that once a process has observed a particular value for a data item, it will never see that value roll back or change to a previous state. This ensures that the system's <u>state transitions are always moving forward</u> in a consistent manner.

Monotonicity is important in distributed systems to maintain consistency and prevent conflicts that can arise from concurrent updates or network partitions. By ensuring that processes never regress to a previous state, monotonicity helps maintain the integrity of the system and its data.

In practical terms, monotonicity can be achieved through mechanisms such as 
- versioning, 
- timestamps,  
or other techniques that track the order of operations and ensure that updates are applied in a consistent and irreversible manner across the distributed system.

## Monotonic Counters

In the context of distributed systems, the term "monotonic counter" refers to a type of counter that <u>only increments</u> or <u>remains the same</u> over time. This means that the value of the counter can only increase or stay constant, but it will never decrease or reset to a lower value.

Monotonic counters are used in distributed systems to track the progress or state of certain operations or events in a way that <u>ensures</u> **consistency** and **prevents conflicts**. 

By maintaining a monotonically increasing value, monotonic counters help avoid issues such as 
- race conditions, 
- conflicting updates, or 
- inconsistencies that can arise in distributed environments.
