
## 1 What is DBMS?

**DBMS (Database Management System)** is software used to create, manage, store, and retrieve data in an organized manner.
Examples: MySQL, PostgreSQL, Oracle.

---

## 2 What is Joins?

**Joins** are used in SQL to combine rows from two or more tables based on a related column.

---

## 3 What are Left and Right Joins?

* **LEFT JOIN** → Returns all records from the left table and matching records from the right table.
* **RIGHT JOIN** → Returns all records from the right table and matching records from the left table.

---

## 4 What is TRUNCATE?

`TRUNCATE` removes all rows from a table quickly.

* Cannot use WHERE
* Faster than DELETE
* Resets auto-increment

---

## 5 What is "self" in Methods?

`self` represents the current object of the class in Python.
It is used to access instance variables and methods.

---

## 6 What are Aggregate Functions?

Aggregate functions perform calculations on multiple rows and return a single value.

Examples:

* `COUNT()`
* `SUM()`
* `AVG()`
* `MIN()`
* `MAX()`

---

## 7 What are Inner and Outer Joins?

* **INNER JOIN** → Returns only matching records from both tables.
* **OUTER JOIN** → Returns matching and non-matching records (LEFT, RIGHT, FULL).

---

## 8 Difference Between TRUNCATE and DROP

| TRUNCATE                | DROP                           |
| ----------------------- | ------------------------------ |
| Removes all rows        | Deletes entire table           |
| Table structure remains | Table structure removed        |
| Faster                  | Removes everything permanently |

---

## 9 What is Recursion?

Recursion is when a function calls itself to solve smaller subproblems.

Example:

```python
def fact(n):
    if n == 0:
        return 1
    return n * fact(n-1)
```

---

## 10 Example for SQL and NoSQL Databases

* **SQL Database** → MySQL, PostgreSQL (Structured tables, fixed schema)
* **NoSQL Database** → MongoDB, Cassandra (Flexible schema, document-based)

---

## 11 What is String Concatenation?

Combining two or more strings.


SQL:

```sql
SELECT CONCAT('Hello', 'World');
```

---

## 12 What is a Function in Python?

A function is a reusable block of code that performs a specific task.

Example:

```python
def greet(name):
    return "Hello " + name
```

---

## 13 Difference Between Shallow Copy and Deep Copy

| Shallow Copy                       | Deep Copy                             |
| ---------------------------------- | ------------------------------------- |
| Copies reference of nested objects | Copies entire object including nested |
| Changes affect original            | Changes do not affect original        |

---

## 14 Difference Between DROP and DELETE

| DELETE                                 | DROP                    |
| -------------------------------------- | ----------------------- |
| Removes specific rows (WHERE possible) | Removes entire table    |
| Can rollback (transaction dependent)   | Usually cannot rollback |
| Structure remains                      | Structure removed       |

---

## 15 How to Extract Month from Datetime?

SQL:

```sql
SELECT EXTRACT(MONTH FROM date_column);
```

PostgreSQL:

```sql
SELECT date_part('month', date_column);
```

---

## 16 When Do We Use HAVING?

`HAVING` is used with `GROUP BY` to filter aggregated results.

Example:

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```
