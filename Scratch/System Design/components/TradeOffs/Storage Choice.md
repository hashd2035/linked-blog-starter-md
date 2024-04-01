
| Criteria                  | Possible Choice |
| ------------------------- | --------------- |
| Ready Heavy               |                 |
| Write Heavy               |                 |
| Relationship among Tables |                 |
| Strong ACID Consistency   |                 |

## Characteristics of Different Databases
#### MongoDB
- uses leader-follower protocol, making it possible to use replicas for heavy reading.
- ensures atomicity in concurrent write operations and avoids collisions by returning duplicate-key errors for record-duplication issues.

### Cassandra, Riak, DynamoDB
- need read-repair during the reading stage and hence provide slower reads to write performance.
- They are leader-less NoSQL databases that provide weaker data consistency guarantees upon concurrent writes. Being a single leader database, MongoDB provides a higher read throughput as we can either read from the leader replica or follower replicas. The write operations have to pass through the leader replica. It ensures our system’s availability for reading-intensive tasks even in cases where the leader dies.


## References
https://www.educative.io/courses/grokking-modern-system-design-interview-for-engineers-managers/design-and-deployment-of-tinyurl