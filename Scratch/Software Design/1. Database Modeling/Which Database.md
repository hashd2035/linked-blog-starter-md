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
