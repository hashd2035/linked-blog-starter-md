```toc
```

[[Database Interview]]

## Database Toolbox
Keep at least one of each in your interview toolbox
Databases for 
- Transaction (RDBMS)
- Search 
	- Elastic Search
	- Reversed Index
- Low-Latency 
- Long-Term storage 
- Ephemeral storage 
- Time series 
	- [Youtube: InfluxDB: The Basics of Time Series Data](https://www.youtube.com/watch?v=wBWTj-1XiRU&pp=ygUUdGltZSBzZXJpZXMgZGF0YWJhc2U%3D)
- The cloud 
- On-premises 
- Reducing costs 
- Analytics 
- Grouping 
- Big Data 
## Types of Databases

### Relational Databases
[[Why Relational databases]]
### NoSQL
designed to handle unstructured or semi-structured data and offer more flexible schema
#### Use Cases:
- JSON Document Stores
	- e.g. MongoDB, Couchbase
- Key Value Stores
	- Be careful when using KV Stores, because they could be a limit on the size of the value you can put in.
	- e.g. DynamoDB (2~4KB), Redis
- Column-Family Stores
	- Optimal for managing and analyzing large amounts of data, especially in wide-column stores
	- e.g. Cassandra, HBase
- Graph Databases
	- Perfect for data with complex relationships, like social networks and recommendation engines
	- e.g. Neo4j, Amazon Neptune
#### Some comparisons
##### MongoDB vs RDBMS

|                           | RDBMS                                      | MongoDB                                                 |
| ------------------------- | ------------------------------------------ | ------------------------------------------------------- |
| Type                      | relational databse                         | non-relational database and document oriented databacse |
| hierarchical data storage | Not suitable for hierarchical data storage | Suitable for hierarchical data storage                  |
| Scalability               | vertically scalable i.e increasing RAM     | horizontally scalable i.e add more servers.             |
| Schema                    | predefined schema                          | dynamic schema                                          |
| Security                  | quite vulnerable to SQL injection          | not affected by SQL injection                           |
|                           | centers around ACID properties             | centers around the CAP theorem                          |
|                           | row-based                                  | document-based                                          |
|                           | slower in comparison with MongoDB          | almost 100 times faster than RDBMS                      |
| Join                      | Supports complex joins                     | No support for complex joins                            |
|                           | column-based                               | field-based                                             |

#### In Memory Databases 
In-Memory database store data in the main memory, offering rapid data access and reduced latency
##### Use cases:
- Real-time analytics, 
- Caching frequently accessed data, Distributed Cache 
- High-performance applications
##### Examples: 
Redis, SAP HAHA, Memcache
### Columnar Databases
store data in columns rather than rows, which enhances query performance for analytics
- Sometimes involve denormalizing your data
- Aggregating data is cheaper (avoids Joins) 
##### Use cases:
- Data warehousing
- Business Intelligence
- Complex Reporting
##### Examples:
Amazon Redshift, Google Big Query

Note: A column-family data model is not the same as a column-oriented model
- A column-family database (e.g. Cassandra) stores a row with all its column families together, whereas a column-oriented database (or Columnar database such as Redshift) simply stores data tables by column rather than by row.
### Time Series Databases
efficiently store and retrieve time-stamped data points, often used for monitoring and IoT applications
##### Use cases:
- Sensor data analysis
- Monitoring systems
- Financial market data analysis
##### Example:
InfluxDB, OpenTSDB
### Spatial Databases
specialize in managing spatial and geographic data, enabling location-based queries
##### Use cases:
- Geographic Information Systems (GIS)
- Mapping Applications
- Location-based Services
##### Examples:
PostGIS, Oracle Spatial
### Graph Databases
are designed to store and manage interconnected data using nodes and edges
##### Use cases:
- Social Networks
- Recommendation Systems
- Fraud Detection
##### Examples:
Neo4j, ArangoDB
### NewSQL Database
aim to combine the benefits of traditional relational databases with those of NoSQL databases, focusing on scalability and performance
##### Use cases:
- Large applications requiring ACID compliance and horizontal scalability
##### Examples:
Spanner, Cochroaches, NuoDB
## Choosing the Right Database
### Factors to consider
<u>Data structure</u> (Schema), <u>query complexity</u>, <u>scalability</u>, <u>data volume</u>, <u>performance requirements</u>, <u>Consistency needs</u>, <u>budget</u>, and <u>future growth plans</u>
### Key Takeaway
Selecting the appropriate database type is crucial for optimizing data management and achieving desired application performance.


## Case Study: Web Crawler
Design a storage solution for a web-crawler that scrapes the product and pricing information from a competitor's e-commerce website. Describe how you handle the data you collect.

#### What criteria should we be looking at
- What kind of data are we dealing with?
	- Do we need strong consistency or ACID compliance? 
		- If yes, RDBMS
		- If no, then, is eventual consistency okay? NoSQL is also possible 
	- Is this relational data, if they are, do we have many relationships? 
		- If yes, as in ECommerce, then RDBMS
		- If not, but, not many, then, NoSQL is also possible
	- Do we have a predictable schema?
		- Does schema needs to be flexible?
		- Could there be missing fields?
		- If yes to above two, RDBMS is not the right choice
			- Or, we'll have to do some sort of post processing to make sure the data is useful and fit into database
	- Do we need to store media blobs? 
	- Do we need to store JSON?	
	* Do we need to store the original HTML pages?
		* S3?
	* Do we need to store meta data? 
- What is the use case?
	- Further analytics? 
		- like data warehousing? Columnar database
		- AI? Vector DB?
	- Will the data be served by another set of customers in online fashion? 
		- Query Complexity?
		- Read/write ratio?
		- should look at non functional requirements
* What non functional requirements do we have?
	* What kind of scraping are we doing?
		* Are we scraping the whole page and then run some AI or Analysis at the later stage?
		* Or, are we simply interested in few fields (e.g. Product Name and Pricing) for a specific website (e.g. Amazon)?
		* How many products? 
			* If 10 million products, then, that is actually very small number, we can just use RDBMS
	* How many incoming data? What are the throughput? Write per sec?
		* If lots of data needs to be written fast, should be write optimized
		* If lots of data needs to be read fast, should be read optimized
	* What kind of dataset?
		* Will data be large? Scraped data may be quite big
	* Current Scale, Future Growth? 
		* If massive, then, NoSQL for horizontal scaling
	* What is our clustering strategy?
	* Caching Requirements? Or, how often will the scraper being run?
		* can recache it 7 days - update delay is permitted
		* or, wants to recache and scraping immediately - I want a real time update
			* it will require a lot more infrastructure and be expensive
* What is read/write ratio?
	* Read optimized - RDBMS, MongoDB (uses B-tree)
	* Write optimized - Cassandra, DynamoDB 

#### What are the use cases?
- Store / retrieve products by title, product id, other search term
- Compare pricing in models (simple, <u>hierarchical</u> based on features)
	- Product has product detail
	- Variation has colors, sizes, etc.
	- Joining the table to represent hierarchical data vs. hierarchical in nature  
- Serve Images and metadata
- Deduplicate products / determine and avoid cycles
	- We may want to understand how scraping works before considering the database options
- DFS / BFS in scrape exploration
	- That will change in-memory requirement
- Product similarity graph / similarity search
	- Vector Database?
#### Database size calculation
- Assume 10 million unique product pages
- Average page size = 2MB
- Blob storage size = 10 million * 2MB = 20 TB
- Images can be stored in CDN (e.g. S3) and can be referred to via URLs
- Row size 
	- url (50 bytes), hash (16 bytes), blob (16 bytes), title (60 bytes), description (150 bytes), last updated (8 bytes) Total = 300 bytes
- 10 million rows = ~ 3GB of document storage
- Can be easily stored in horizontally scalable MongoDB cluster
#### HLD
![[Which Database 2024-04-11 10.53.34.excalidraw]]

#### Observations
- Combined strengths of various databases / storage solutions
	- Sometimes, we may <u>not have this luxury</u> and we may have to come up with alternate solution
- <u>Sharded requests</u> by design (e.g. data and CDN resources on separate paths)
- Hosted solutions that <u>scale horizontally</u> (e.g. DynamoDB, Redis, Elastic Search)
- <u>Eventual consistency</u> as and when pages are scraped and indexed


## Case Study: The payment system from Google Play store
https://uplevel.interviewkickstart.com/resource/associated-class-video-706812-1524-47255-1
1:39:55

Design the payment system for the Google Play store. Define the type of database you would use and why? Design entity and relationships that satisfy storage requirements


## Case Study: Social Media website
3:12:12

Select a database type(s) for a social media website that includes search, user connections, user feeds, ads as well as payments. Design for scalability given peak events and hours. Design ER diagram for a subsection of the entities indicating entities , relationships and constraints.

## Case Study: 
3:28:33

Design a data warehousing solution for an ecommerce website where metrics regarding product sales and customers are required on various frequencies (hourly, daily, monthly, quarterly and yearly). Ref. Shopify API: https://shopify.dev/api

## Database Design Assignment

 List clarifying questions you would ask the interviewer. Interviewers often give interviewees incomplete information. They expect you to ask the questions necessary to solve the problem.
 Answer the clarifying questions posed in part 1. State your assumptions. Answer your own questions for now.

Describe the architecture of your solution at a high level. 
Databases are part of the larger system architecture. What does the overall system architecture look like? What are the data flows? Will you have APIs, queues, streams, etc? It could be helpful to draw some diagrams, along with writing notes. Then, identify where database systems will be necessary to manage data.

List the databases your design requires. 
For example, your design may require three (any number of databases, really) databases, and you choose SQL, ElasticSearch, and MongoDB.

- For each database, list the requirements. The requirements include latency, size, transactional/consistency requirements, update frequency, etc.
- For each database, describe the data the database will contain. Will the data have a fixed schema? Is the data relational or unstructured? You may find it helpful to diagram the schema and think about fields and relations.
- For each database, explain why you chose that system over other options. For example, say you choose a SQL relational database for a specific use case. What are the advantages of using that traditional relational database over using a NoSQL option? Consider possible alternatives. What are the advantages of your database choice over others? Advantages may include cost, latency, scalability, simplicity, security, etc.

### Question 1: Design LinkedIn’s messaging system

##### FR / Use cases
1. 1:1 messages (not group chatting) with multiple people
	1. Messages (causal ordering) should be in order -> Vector clock (sequence)
2. can share contact info 
3. User side and Recruiter side may be different
4. attach file (e.g. resume)
5. History never gets deleted
6. Most recent chat get to the top (recently used order is important)
	1. Top 10 or 20 are shown. Others are shown when scrolled down
7. Push Notification when some one messaged 
8. Read receipt?
9. Comments on msg? Reply to a certain thread/message

##### **Non Functional Requirement****
1. Causal ordering is important, but, eventual consistency is okay
2. High availability, Reliability, Durability 
3. Scalability
4. Low Latency?

##### **API** (ask question how would you implement this - system design / data query)
- sendChat(sender, receiver, msg) -> chatId, msgId
- sendChat(chatroomId, msg, attachment) -< msgId
- shareContact(chatroomId, msg)
- getRecentChat(pagination)
- search chat?
- 

##### **Data Model**
Note: when designing data model, think how we would query the data we need. Also, rationale behind each attributes.
- ChatRoom (chatRoomId: PK/NN, createdDateTime, lastModifiedDateTime)
	- Message (messageId: PK/NN, chatRoomId: FK/NN, seq: Integer/NN, dateTime)
- ChatRoomHistory (memberId, chatRoomId: PK/NN, seq, lastModifiedDateTime)
- Members (memberId: PK/NN, memberLinkedInAddress: NN, )
- Followers (memberId: PK, followerId: FK)
- MemberContactInfo (memberId: PK, phoneNumber, email, linkedInAddress)

**ERD**
![[Which Database 2024-04-11 16.21.28.excalidraw]]
Some impacts of this model
- If you have a graph like that: bob follows judy, judy follows bob you may end in an endless loop.
- If you want to find followers of followers ... you have to query several times. There are some 
vendor specific extensions for recursive queries, but plain ANSI SQL doesn't support this 
(and so your OR Mapper will no support it out of the box).

My point of view: 
- It is a model, where a relational database doesn't fit well. 
- A graph DB, like neo4j is a better choise for that case.

This is why data modeling along with choosing database should happen after HLD
##### HLD

![[Which Database 2024-04-11 16.45.35.excalidraw]]


#### Discussion 
##### How would you write a query to find out which senders: receiver.
Document Store? Maybe 
- My take is (In-memory) key/value store, but, ordering preprocessing happens
	- Append only,  
	- userid1-userid2-creationTimeStamp as document id ??
- What if there are lot of messages, so, document in document database 
- Time series makes sense too
- RDBMS could be good for Chat system where you can order the rows in fairly cheap fashion. 
- Can use append only chunks as raw files
##### How to figure out who I have chat recently?
- Last_modified_date


##### Ashish Kaila's take
![[Pasted image 20240411184241.png]]
![[Pasted image 20240411184336.png]]
![[Pasted image 20240411184455.png]]
![[Pasted image 20240411184729.png]]
### Question 2: Design S3
https://highscalability.com/behind-aws-s3s-massive-scale/

GFS/HDFS, DynamoDB

Pros and Cons of Time Series, Use cases, How they are actually used