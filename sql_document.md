

## 1. ACID Properties

ACID properties define how reliable transactions are handled in relational databases.

* **Atomicity** means a transaction is all-or-nothing. If any step fails, the entire transaction is rolled back.
* **Consistency** ensures that the database always moves from one valid state to another. It never violates constraints.
* **Isolation** ensures that multiple transactions running at the same time do not interfere with each other.
* **Durability** guarantees that once a transaction is committed, the changes are permanently stored, even if the system crashes.

In simple terms, ACID makes sure your data is safe and reliable during transactions.

---

## 2. CAP Theorem

The CAP Theorem applies to distributed systems. It states that you can only guarantee two out of the following three properties:

* **Consistency** – Every read gets the most recent write.
* **Availability** – Every request gets a response.
* **Partition Tolerance** – The system continues working even if there is a network failure between nodes.

In real-world distributed databases, Partition Tolerance is mandatory, so systems usually choose between:

* CP (Consistency + Partition Tolerance)
* AP (Availability + Partition Tolerance)

You cannot have all three at the same time.

---

## 3. Joins

Joins are used to combine data from multiple tables based on a related column.

Common types:

* **INNER JOIN** – Returns only matching records from both tables.
* **LEFT JOIN** – Returns all records from the left table and matching records from the right.
* **RIGHT JOIN** – Returns all records from the right table and matching records from the left.
* **FULL JOIN** – Returns all records from both tables, whether matched or not.

Joins are essential when working with normalized databases where data is split across multiple tables.

---

## 4. Aggregations and Filters in Queries

Aggregation functions are used to perform calculations on groups of rows.

Common aggregate functions:

* COUNT()
* SUM()
* AVG()
* MIN()
* MAX()

When filtering data:

* **WHERE** is used before grouping (filters individual rows).
* **HAVING** is used after GROUP BY (filters aggregated results).

For example, if you want departments with more than 5 employees, you use HAVING.

---

## 5. Normalization

Normalization is the process of organizing data to reduce redundancy and improve data integrity.

The main normal forms:

* **1NF (First Normal Form)** – Each column contains atomic values and no repeating groups.
* **2NF (Second Normal Form)** – Removes partial dependency on composite keys.
* **3NF (Third Normal Form)** – Removes transitive dependency (non-key depending on non-key).

The goal of normalization is to:

* Avoid duplicate data
* Prevent update anomalies
* Maintain clean structure

---

## 6. Indexes

Indexes improve the speed of data retrieval.

They work like an index in a book — instead of scanning every row, the database can quickly locate the required data.

Indexes are commonly created on:

* Columns used in WHERE
* Columns used in JOIN
* Columns used in ORDER BY

However:

* They improve read performance.
* They slightly slow down insert, update, and delete operations.
* They consume extra storage.

So indexes should be used strategically.

---

## 7. Transactions

A transaction is a group of SQL operations treated as a single unit of work.

The main commands are:

* BEGIN
* COMMIT
* ROLLBACK

If something goes wrong, ROLLBACK undoes all changes made in that transaction. If everything is successful, COMMIT saves the changes permanently.

Transactions ensure data integrity.

---

## 8. Locking Mechanism

Locking is used to control concurrent access to data.

When multiple transactions try to access the same data:

* A **Shared Lock** allows reading but not modifying.
* An **Exclusive Lock** allows modifying and prevents others from accessing it.

Improper locking can cause:

* Blocking
* Deadlocks

Databases automatically manage locking to maintain consistency.

---

## 9. Database Isolation Levels

Isolation levels define how transactions behave when running simultaneously.

There are four main levels:

* **Read Uncommitted** – Can read uncommitted data (dirty reads possible).
* **Read Committed** – Can only read committed data.
* **Repeatable Read** – Rows read cannot change within the transaction.
* **Serializable** – Highest level. Transactions behave as if executed one after another.

Higher isolation increases consistency but may reduce performance.

---

## 10. Triggers

Triggers are special database procedures that automatically execute when certain events occur.

They can be triggered on:

* INSERT
* UPDATE
* DELETE

Common use cases:

* Audit logging
* Maintaining timestamps
* Enforcing business rules
* Data validation

Triggers run automatically without manual intervention.



