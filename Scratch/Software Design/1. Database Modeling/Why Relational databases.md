```toc
```

# Relational Database
A database is a structured collection of data that enables efficient **<u>storage</u>**, **<u>retrieval</u>** and **<u>management</u>** of information.
## Relation Data Model
is a structured way of organizing data using tables with entities, attributes and relationships
### Key Principles
- Entities - represent object (e.g. can be more than one table)
- Attributes - describe the properties of entities (e.g. columns of the table)
- Relationships - define how entities are connected
### Advantages of the Relational Model
- Relational databases offer benefits such as <u>data integrity</u>, <u>flexibility</u>, and<u> scalability</u> due to their well-defined structure and standardized query language (SQL)
### Advantages and Limitations of Relational Databases
##### Benefits of Relational Databases
- Relational databases 
	- ensures data accuracy, 
	- enable data modification without compromising integrity, and 
	- can be scale to accommodate large datasets and complex queries
##### Limitations (Complexity, Performance Consideration)
- Despite their strengths, relational databases can be complex to design and maintain and in some cases, performance may be impacted with very large datasets or complex joins 
##### The dataset might not be always structured i.e. not all kinds of data can be put in RDBMS

### ACID (Atomicity, Consistency, Isolation, Durability) Properties 
ACID (Atomicity, Consistency, Isolation, Durability) is a set of properties  that guarantee the reliability and integrity of transactions in a relational database management system (RDBMS). These properties help differentiate RDBMS from NoSQL alternative, which often prioritize flexibility and scalability over strict ADIC compliance.
- Atomicity - All transaction either succeed or fail (rollback)
- Consistency - related to Referential Integrity
- Isolation 
- Durability

|             | Relational Databases                                                                                                                                                                 | NoSQL                                                                                                                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Atomicity   | Either all the changes within a transaction are applied, or none are applied                                                                                                         | Some NoSQL databases support atomic operations within a single document or record, but, they may not offer the same level of transactional support across multiple documents or records           |
| Consistency | If a transaction violates a <u>constraints</u>, it is rolled back                                                                                                                    | NoSQL databases often relax consistency in favor of high availability and performance                                                                                                             |
| Isolation   | RDBMS system provide strong isolation between concurrent transactions, ensuring that one transaction's <u>operations are not visible to others until it's completed</u>              | NoSQL databases may sacrifice stronger isolation guarantees, especially in distributed environments, in exchange for improved performance, contrasting with the stricter isolation of RDBMS       |
| Durability  | RDBMS systems guarantee durability by <u>persisting committed transactions to non-volatile storage</u> (e.g. disk) to ensure data is not lost, even in the event of a system failure | NoSQL database differ in durability features. Some offer default durability, while others permit users to tailor it. Occasionally, NoSQL databases prioritize performance over instant durability |
Note: 
- <u>Constraints</u> - is data missing, is the data well formatted, Does it need trigger, etc. You can put a constraints on transaction which is useful in especial ML where you can clean the data before even it is put into the database.
- Referential Integrity 

## Uses
ECommerce, HR/Accounting System, Financial/Banking System 

