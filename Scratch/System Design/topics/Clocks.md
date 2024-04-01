```toc
```

## Physical Clocks
There are often two types of physical clocks available in a computer: 
- the time-of-day clock and 
- monotonic counters.
### The time-of-day clock
- Usually has lower resolution in comparison to monotonic counters
- Network Time Protocol (NTP) can move the clock forward or backward, so it’s **<u>not always monotonic</u>**.
- may or may not incorporate leap seconds.
### Monotonic Counters
[[Monotonicity#Monotonic Counter]]

* Monotonic counters usually have higher resolution than time-of-day clocks.
- Monotonic counters <u>should be used for the duration between two events</u> <u>rather than for the time</u>.
- These aren’t meaningful across different nodes. 
	- For instance, even on the same server with multiple processors, there can be a different counter per processor. The application needs to be careful when using counters from different processors.
- The NTP might adjust it without violating monotonicity.
- The NTP can only speed up or slow down the counter rate of change by up to 0.05%.
### Reasons for clock drift

Physical clocks drift over time due to many reasons:

- Temperature differences
- The equipment’s age
- Manufacturing defects
- Virtualized clocks
### The trade-off

It’s possible to keep clock drift consistently small using GPS and atomic clocks, careful deployment, and monitoring. However, such a system comes with an added dollar cost, as well as increased system complexity.
### Summary

- Due to factors like network latency and hardware differences, they might not be perfectly synchronized across the system.
- Not reliable for determining the causal ordering of events in a distributed system.
## Logical Clocks

### Lamport clocks

- Lamport clocks provide us with **happened-before** relationships. 
	- If event A happens before event B, then the clock value of A will be less than the clock value of B. 
	- There’s a subtle point that given any two clock values of two events from any two servers, we can’t compare them to infer the happened-before relationship because those two events can be concurrent (meaning not causally related).

- assigns a monotonically increasing counter value to each event.
- Useful for detecting causality (e.g., event B happened after event A), but not for determining the exact order of concurrent events.
### Vector clocks

- We can use vector clocks to infer the **happened-before** relationships using the clock values. For this, we’ll need a counter per participating entity in the vector.
- We should <u>note that happened-before might not mean that two events were causally related</u>. 
	- It might be the case that one event happened before the other.
	- Usually, we need application-level context on top of the happened-before mechanism to infer real causality.
	
- assign timestamps to each process/server in the system as a vector.
- Each entry in the vector represents the logical time at a specific process.
- Allows for partial ordering of events, even those happening concurrently on different servers.
### **Importance of Logical Clocks:**

- **Event Ordering:** Logical clocks help determine the causal relationship between events in a distributed system, even with imperfect physical clock synchronization.
- **Concurrency Control:** They are crucial for implementing concurrency control mechanisms, ensuring data consistency when multiple processes access shared resources.
- **Causal Delivery:** In message passing systems, logical clocks enable causal delivery, ensuring messages are delivered in the order they were causally sent, even if they arrive out of order due to network delays.

### Relationship with [[2PC]], 3PC, Atomic Operations, and Consistency Models

- **2PC (Two-Phase Commit) and 3PC (Three-Phase Commit):** These are protocols used to ensure data consistency in distributed transactions. Logical clocks can be used alongside these protocols to track the order of operations within the transaction across multiple servers.
- **Atomic Operations:** Logical clocks can be used to verify that atomic operations (indivisible actions) have completed successfully in the desired order across the system.
- **Consistency Models:** Different consistency models (e.g., eventual consistency, strong consistency) have varying requirements for event ordering. Logical clocks can play a role in achieving the desired consistency guarantees.

### Usage in Messenger Message Ordering

In messaging systems, logical clocks are crucial for ensuring messages are delivered in the order they were sent, preserving causality. This is especially important for applications where the order of events matters, such as chat conversations or financial transactions. By using vector clocks or other logical clock mechanisms, messages can be stamped with timestamps that reflect their causal ordering, even if they arrive out of order due to network delays.

### Additional Considerations

- Choosing the right type of logical clock depends on the specific needs of the distributed system. Lamport timestamps are simpler but offer less information, while vector clocks provide more detailed ordering but are more complex to manage.
- Logical clocks are a tool for reasoning about event ordering and consistency in distributed systems. They don't replace physical clocks entirely, but rather provide a way to overcome their limitations in a distributed environment.

By understanding different types of clocks and their applications, you can build more robust and reliable distributed systems that ensure data consistency, causal ordering of events, and efficient message delivery.