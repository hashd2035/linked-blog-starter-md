https://hasura.io/learn/database/mysql/core-concepts/3-schema-ddl-dml/
## DDL
Schema (e.g. Table) Level
```sql
CREATE TABLE employee_table(
	id int NOT NULL AUTO_INCREMENT,
	name varchar(45) NOT NULL,
	occupation varchar(35) NOT NULL,
	age int NOT NULL,
	PRIMARY KEY (id)
);

DROP TABLE orders;

ALTER TABLE cus_tbl
ADD cus_age varchar(40) NOT NULL;

TRUNCATE TABLE customer;
```

## DML
```sql
INSERT INTO People VALUES
(102, 'Joseph', 'Developer', 30),
(103, 'Mike', 'Leader', 28),
(104, 'Stephen', 'Scientist', 45);

UPDATE trainer
SET email = 'mike@sql.com'
WHERE course_name = 'MySQL'

DELETE FROM Employees WHERE emp_id=108
```

## DQL

```sql
SELECT * FROM Customers;
```
## DCL
 deal with the rights, permissions and access control of the database system.
 - GRANT
 - REVOKE

## TCL
deal with the transaction within the database.
- COMMIT
- ROLLBACK
- SAVEPOINT
  SET TRANSACTION

```sql

```