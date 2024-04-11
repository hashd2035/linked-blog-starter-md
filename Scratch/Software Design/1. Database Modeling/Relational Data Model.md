## Entities and Attributes
- Entities - represent real-world objects or concepts (e.g. "Customer", or "Product")
- Attributes - describe the properties of these entities (e.g. "Customer Name", "Product Price")
- Primary Keys - are <u>unique</u> identifiers for entities, ensuring each record in a table is distinct (e.g. "StudentID" as the primary key for the "Student" entity)

![[Pasted image 20240409210639.png]]

## Relationships
- Relationships define how entities are connected in a database, such as how students are related to courses they enroll in
- These describe the cardinality of relationships - whether one entity can be associated with one or many instances of another entity (e.g. one customer can place many orders)
- One-to-One, One-to-Many, and Many-to-Many
![[Pasted image 20240409212144.png]]
- In the above diagram, entities are rectangles, and relationships are diamonds.
## Keys in Relational Databases
- Primary Keys
	- uniquely identified records within a table, such as  social security number (bad practice, though, since ssn needs to be encrypted and should not be exposed) for individuals or a product ID for products
- Candidate Keys and Super Keys (Composite primary key)
	- We could have more than one way to uniquely identify records
		- Candidate keys are potential primary keys
		- Super keys are combinations of attributes that uniquely identify records
			e.g.
	- We choose one of them to be the primary key

note: creating composite primary key in mysql
```sql
		CREATE TABLE person (
		   P_Id int ,
		   ............,
		   ............,
		   CONSTRAINT pk_PersonID PRIMARY KEY (P_Id,LastName)
		);
```

- Foreign Keys
	- establish relationship between tables, pointing to the primary key in another table and enforcing <u>referential integrity</u> by ensuring data consistency and preventing orphaned records. 
	- Referential integrity (also, known as <u>foreign key constraints</u> ) is a database design constraint that ensures that each foreign key in a table points to a unique primary key value in another table. 

![[Pasted image 20240409214352.png]]
You cannot have an `order` without `customer_id`, if there is one, then, it's breaking referential integrity. 

## Data Integrity and Constraints
- Ensuring Data Accuracy and Consistency
	- <u>Data Integrity</u> in vital and <u>constraints</u> are rules applied to fields. e.g. 
		- `NOT NULL` enforces the presence of data, 
		- `UNIQUE` ensures values are unique and 
		- `CHECK` defines custom validation rules
- Constraints
	- `NOT NULL`, `UNIQUE`, `CHECK`, `DEFAULT` - these constraints contribute to data quality by preventing data anomalies and errors
- Constraints ensure data consistency and reliability, reducing the risk of errors and inconsistencies in the database. 
## Importance of Data Constraints
1. Improved Data Quality
	- constraints lead to better data quality and informed decision-making
2. Reduced Maintenance Effort
	- constraints reduce data corruption and the need for manual cleanup
3. Enhance Communication
	- constraints document rules and facilitate communication among stakeholders
![[Pasted image 20240409221221.png]]






