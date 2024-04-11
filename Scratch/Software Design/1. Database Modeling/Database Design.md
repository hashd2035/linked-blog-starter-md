```table-of-contents
```
## Phases of database design
There are 4 phases of the database design
- Requirements
- Conceptual Design
- Logical Design
- Physical Design

### Step1: Requirement Gathering
Gather detailed requirements from stakeholders and end-users
- **Customer Needs**: Understand what customers expect in terms of product selection, search capabilities and ordering options
- **Inventory Management**: Determine how inventory tracking should work, including restocking triggers
- **Payment and Check out**: Define payment methods, security measures and the checkout process
- **User Accounts**: Identify the information required for customer profiles and registration
- **Delivery**: Clarify delivery preferences, locations, and scheduling options

### Step2: Conceptual Design
Translate gathered requirements into a high-level, abstract conceptual model
- Entities: identify primary entities like "Product", "Customers", "Orders" and "Inventory'"
- Attributes: Define attributes for each entity. e.g. "Product Name", "Customer Address", "Order Date"
- Relationships: Establish connections between entities. e.g. "Customer Place Orders", "Products & Customers are part of Orders" 
	- Entity <u>verb</u> Entity

### Step3: Logical Design
Refine the conceptual model into a more detailed logical design
- Tables
	- Create tables for each entity identified in the conceptual model, specifying fields (attributes)
- Data Types
	- Define data types for fields, such as text, numeric, date, or Boolean
- Constraints
	- Implement data integrity constraints like primary keys, foreign keys and unique constraints
- Normalization
	- Apply <u>normalization</u> techniques to optimize the structure, reducing data redundancy and ensuring efficient data storage
### Step 4: Physical Design
Transform the logical design into a practical database implementation
- DBMS selection
	- Choose a suitable DBMS like MySQL, PostgreSQL, or others based on system requirements and scalability
- <u>Indexing</u>
	- Determine which fields require indexing for faster query performance
- <u>Partitioning</u>
	- If dealing with large datasets, consider data partitioning strategies
- Security
	- Implement robust security measures to protect customer data
- Performance Tuning
	- Optimize database performance through techniques like query optimization and caching

## Data Governance

## ERD
- Entities - represent real-world objects or concepts 
- Attributes - properties or characteristics of entities
- Relationships - connection between entities
- Cardinality - the number of related records between entities

![[Pasted image 20240409230607.png]]
## Normalization Techniques for Efficient Databases

![[Pasted image 20240410102426.png]]

### Insert Anomaly
![[Pasted image 20240410102527.png]]
### Update Anomaly
![[Pasted image 20240410105008.png]]

Note: TPC (Transaction Processing Performance Council) is an industry standard benchmark for measuring the performance of online transaction processing (OLTP) systems. TPC benchmarks are used to measure the performance of computing environments.
- TPC-C - This benchmark is measured in transactions per minute (tpmC) and represents any industry that must manage, sell, or distribute a product or service.
- TPC-DS - This benchmark models aspects of a decision support system, such as queries and data maintenance. It provides a representative evaluation of performance as a general purpose decision support system.
- TPC-E - This benchmark models a brokerage firm with customers who generate transactions related to trades, account inquiries, and market research.
### Delete Anomaly
![[Pasted image 20240410120910.png]]
## Levels of Normalization
- **First Normal Form (1NF)** - Eliminates <u>duplicate columns</u> in a table
- **Second Normal Form (2NF)** - Ensures non-key attributes are fully functionally dependent on the <u>primary key</u>
- **Third Normalization (3NF)** - Removes <u>transitive dependencies</u> between non-key attributes and enforces independent relationships
- **Boyce-Codd Normal Form (BCNF)** - Eliminates <u>partial dependencies</u> in a table

### First Normal Form (1NF)
1. In the initial unnormalized state, the `CustomerAddress` field is not atomic (indivisible) because it includes `Street`, `City`, and `Postal code`
2. To achieve 1NF, we split `CustomerAddress` into separate attributes: `CustomerStreet`, `CustomerCity` and `CustomerPostalCode`
3. The same goes for the `Product` table; we split attributes like `ProductName`, `Description`, `Price` into <u>separate columns</u>
### Second Normal Form (2NF)
1. In the initial state, there's a composite primary key (`OrderID` and `ProductID`) in the `OrderDetails` table, and both attributes depend on the whole primary key
2. To achieve 2NF, we create <u>separate tables</u> for `Customers`, `Orders` and `Products`
3. The `OrderDetails` table now <u>reference</u> `Customers` and `Products` using <u>foreign keys</u>, eliminating <u>partial dependencies</u>
### Third Normalization (3NF)
1. In the initial state, Supplier information (`SupplierName`, `SupplierEmail`, `SupplierPhone`) is tied to the `Product` table
2. To achieve 3NF, we create a separate `Suppliers` table with unique `SupplierID`, `SupplierName`, `SupplierEmail` and `SupplierPhone`
3. We modify the `Products` table to <u>reference</u> Suppliers using the `SupplierID`, removing <u>transitive dependencies</u>
### Boyce-Codd Normal Form (BCNF)
1. To achieve BCNF, we introduce a new table, `ProductSupplier` with `ProductID` and `supplierID` as attributes
2. This new table ensures that all functional dependencies are based on <u>super keys</u>
3. Now the `Products` table and the `Suppliers` table are in BCNF, and the database is fully normalized

Many people stop at 3NF, but, there are 4NF, 5NF and 6NF, (7 Levels) and more... 

By applying these normalization steps to the relevant fields data for Fresh Cart, we ensure <u>data accuracy</u>, <u>minimize redundancy</u> and <u>maintain data integrity</u> in the database structure.

## Final Database Fields for Fresh Cart

![[Database Design 2024-04-10 12.49.21.excalidraw]]

## Case Studies

### 1. Fresh Cart
Fresh cart is a well-established online grocery delivery service operating in a business urban area. They faced significant challenges in managing their growing customer base, product inventory and order processing efficiently. These challenges prompted them to transition from manual record-keeping to a robust relational database system

Design a ER diagram for Fresh Cart
#### Entities & Attributes
- Customer: CustomerID (PK), FirstName, LastName, Email (Unique), Phone
- Address: AddressID (PK), Street, City, PostalCode, CustomerID (FK)
- Orders: OrderID (PK), CustomerID (FK), OrderDate
- OrderDetails: OrderDetailID (PK), OrderID (FK), ProductID (FK), Quantity, TotalPrice
- Products: ProductID (PK), Name, Description, Price, StockQuantity, Category, SupplierID (FK)
- Suppliers: SupplierID (PK), Name, Email, Phone
- Promotions: PromotionID (PK), Name, Description, StartDate, EndDate
#### Relationships
- Each customer can have multiple Addresses (billing and shipping addresses)
- Each order is associated with one customer
- Each order can have multiple OrderDetails, specifying the products ordered and quantities
- Each OrderDetail is associated with one Product
- Each product is associated with one Supplier
- Promotions are associated with Orders
#### Database Implementation
Fresh Harvest decided to implement a relational database to streamline their operations. Here's how they structured their database:
1. Customers Table: Stored customer information, including names, addresses, emails, and phone numbers. Each customer had a unique customer ID.
2. Products Table: Contained details about the various products Fresh Harvest offered, such as product names, descriptions, prices and stock levels. Each product was assigned a unique product ID
3. Orders Table: Recorded order information, including order IDs, customer IDs, order dates and order statuses
4. OrderDetails Table: Linked orders to specific products. Its contained order detail IDs, order IDs, quantities, and prices.
![[Pasted image 20240410180002.png]]
Note: 
- Customers table should've had AddressID (FK), as, well.
- The above diagram serves as an example. It isn't rigorously normalized

#### Benefits Realized
After implementing the relational databases, Fresh Cart experienced several significant benefits: 
1. Data Integrity
2. Efficient Inventory Management
3. Streamlined Order Processing
4. Scalability

### 2. Social Media Platform
SnapLife is a dynamic and rapidly growing social media platform that focuses on visual content sharing and storytelling. With its increasing user base and evolving features, SnapLife faces need for a robust and well-structured database system to efficiently manager <u>user interactions</u>, <u>posts</u>, <u>comments</u>, <u>likes</u>, <u>follows</u>, <u>tags</u> and <u>messages</u>. To address this challenge, we must design a comprehensive ER diagram for SnapLife, ensuring the platform's complex data relationships are accurately represented and scalable as the platform continues to expand
#### Entities
- User-Post: One-to-Many (a user can create multiple posts, but, each post is created by one user)
- Post-Comment: One-to-Many (a post can have multiple comments, but, each comment belongs to one post)
- Post-Like: One-to-Many (a post can have multiple likes, but, each like is associated with on epost)
- User-Follow: Many-to-Many (users can follow multiple users and each user can be followed by multiple users)
- User-Tag: Many-to-Many (users can be tagged in multiple posts and each post can tag multiple users)
- User-Message: Many-to-Many (users can exchange multiple messages and each message involves two users)
#### Relationships
![[Pasted image 20240410182841.png]]
Note: There might be errors in the above diagram. How would you fix?


## Demo

![[Pasted image 20240410183253.png]]
3:20 Get email address of the lecturer and get the copy of the interview questions.

Keypoints
- Two sided market place
![[Pasted image 20240410184558.png]]
Ask question to Interviewer (esp. Hiring manager)
- So, if you take 2 month, 6 month and 12 month, near, mid and long term, please define for me how I would be most successful, given those time periods.

![[Pasted image 20240410204941.png]]
![[Pasted image 20240410205041.png]]

## Further Research

EDA (Exploratory Data Analysis)
CRISP-DM
Pandas vs SQL, d-tale
PostgreSQL, pgadmin, dvdrental sample database for postgreSQL

David Reed


