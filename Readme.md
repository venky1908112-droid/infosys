# Infosys DSE Interview Preparation – Questions, Answers & Resources

A comprehensive interview preparation handbook for candidates attending the **Infosys Digital Specialist Engineer (DSE)** interview.

## Contents

1. Python Interview Questions and Answers
2. Java Interview Questions and Answers
3. SQL Interview Questions and Solved Queries
4. DBMS Interview Questions and Answers
5. Computer Networks Interview Questions and Answers
6. Operating Systems Interview Questions and Answers
7. Data Structures and Algorithms
8. Project and Resume-Based Questions
9. HR and Managerial Questions
10. Important Learning Resources
11. Final Interview Preparation Checklist

---

# 1. Python Interview Questions and Answers

## Python Fundamentals

### 1. What is Python?

Python is a high-level, general-purpose programming language known for its simple syntax and readability. It supports procedural, object-oriented, and functional programming.

### 2. What are the main features of Python?

- Simple and readable syntax.
- Dynamically typed.
- Interpreted execution model.
- Object-oriented programming support.
- Large standard library.
- Cross-platform compatibility.
- Automatic memory management.

### 3. Is Python compiled or interpreted?

Python is commonly described as an interpreted language. In CPython, source code is first compiled into bytecode, which is then executed by the Python virtual machine.

### 4. What is dynamic typing?

Dynamic typing means variable types are determined at runtime. We do not need to explicitly declare a variable's type.

```python
x = 10
x = "Hello"
```

The same variable can refer to values of different types.

### 5. What are Python's built-in data types?

- Numeric: int, float, complex.
- Sequence: list, tuple, range.
- Mapping: dict.
- Set: set, frozenset.
- Boolean: bool.
- Binary: bytes, bytearray.
- None type: NoneType.

### 6. Difference between List and Tuple?

| List | Tuple |
|---|---|
| Mutable | Immutable |
| Uses [] | Uses () |
| Supports item modification | Does not support item modification |
| Suitable for changing collections | Suitable for fixed collections |

```python
numbers = [1, 2, 3]
numbers[0] = 10

values = (1, 2, 3)
```

### 7. Difference between List, Set, and Dictionary?

- List: Ordered collection that allows duplicates.
- Set: Collection of unique elements.
- Dictionary: Stores key-value pairs.

```python
a = [1, 2, 2]
b = {1, 2, 3}
c = {"name": "Venkat", "age": 21}
```

### 8. What are mutable and immutable objects?

Mutable objects can be modified after creation. Immutable objects cannot be modified after creation.

Examples:

- Mutable: list, dictionary, set.
- Immutable: int, float, string, tuple.

### 9. Difference between `==` and `is`?

- `==` compares values.
- `is` checks whether two references point to the same object.

```python
a = [1, 2]
b = [1, 2]

print(a == b)  # True
print(a is b)  # False
```

### 10. What is type casting?

Type casting converts a value from one data type to another.

```python
x = "100"
y = int(x)
print(y)
```

### 11. Difference between break, continue, and pass?

- `break`: Terminates the loop.
- `continue`: Skips the current iteration.
- `pass`: Does nothing; acts as a placeholder.

### 12. What is list comprehension?

List comprehension provides a concise way to create lists.

```python
squares = [x*x for x in range(1, 6)]
print(squares)
```

Output: `[1, 4, 9, 16, 25]`

### 13. What are lambda functions?

Lambda functions are small anonymous functions defined using the `lambda` keyword.

```python
square = lambda x: x * x
print(square(5))
```

Output: `25`

### 14. What are `*args` and `**kwargs`?

- `*args` accepts a variable number of positional arguments.
- `**kwargs` accepts a variable number of keyword arguments.

```python
def example(*args, **kwargs):
    print(args)
    print(kwargs)

example(1, 2, name="Venkat")
```

### 15. Difference between append() and extend()?

- `append()` adds one object to the end of a list.
- `extend()` adds each element from an iterable.

```python
a = [1, 2]
a.append([3, 4])
# [1, 2, [3, 4]]

b = [1, 2]
b.extend([3, 4])
# [1, 2, 3, 4]
```

## Python Functions and Advanced Concepts

### 16. What is recursion?

Recursion is a technique in which a function calls itself to solve smaller versions of a problem. It requires a base condition to stop recursive calls.

### 17. What is a generator?

A generator is a function that produces values one at a time using `yield`, instead of returning all values at once.

```python
def numbers():
    yield 1
    yield 2
    yield 3
```

### 18. Difference between yield and return?

- `return` terminates the function and returns a value.
- `yield` produces a value and suspends the function, allowing it to continue later.

### 19. What is an iterator?

An iterator is an object that produces values one at a time using `__next__()`. It follows the iterator protocol.

### 20. Difference between iterable and iterator?

An iterable is an object that can return an iterator using `iter()`. An iterator produces the next value using `next()`.

### 21. What is a decorator?

A decorator is a function that modifies or extends the behavior of another function without changing its original code.

### 22. What is exception handling?

Exception handling manages runtime errors so that a program can handle failures gracefully.

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Execution completed")
```

### 23. Explain try, except, else, and finally.

- `try`: Contains potentially risky code.
- `except`: Handles exceptions.
- `else`: Executes if no exception occurs.
- `finally`: Executes whether an exception occurs or not.

### 24. What is file handling?

File handling allows programs to create, read, write, and modify files.

```python
with open("data.txt", "w") as file:
    file.write("Hello Python")
```

The `with` statement automatically closes the file.

### 25. What is JSON?

JSON stands for JavaScript Object Notation. It is a lightweight data-interchange format.

```python
import json

data = {"name": "Venkat", "age": 21}

with open("data.json", "w") as file:
    json.dump(data, file)
```

### 26. What is the GIL?

The Global Interpreter Lock in CPython allows only one thread at a time to execute Python bytecode within a process. It affects CPU-bound multithreaded execution, although threads can still be useful for I/O-bound work.

### 27. Difference between multithreading and multiprocessing?

- Multithreading uses multiple threads within one process and shares memory.
- Multiprocessing uses separate processes with separate memory spaces.
- Multiprocessing is generally more suitable for CPU-bound parallel work in standard GIL-enabled CPython.

### 28. What is garbage collection?

Garbage collection automatically manages memory by reclaiming memory occupied by objects that are no longer needed. CPython primarily uses reference counting, supplemented by cyclic garbage collection.

## Python OOP Questions

### 29. What is a class and an object?

A class is a blueprint that defines attributes and methods. An object is an instance of a class.

```python
class Student:
    def __init__(self, name):
        self.name = name

s = Student("Venkat")
print(s.name)
```

### 30. What is inheritance?

Inheritance allows one class to reuse and extend the properties and methods of another class.

```python
class Animal:
    def sound(self):
        print("Animal sound")

class Dog(Animal):
    pass
```

### 31. What is polymorphism?

Polymorphism means the same interface or method name can behave differently depending on the object or implementation.

### 32. What is encapsulation?

Encapsulation combines data and related methods inside a class and controls how the internal state is accessed.

### 33. What is abstraction?

Abstraction hides implementation details and exposes only essential functionality. Python supports abstraction through abstract base classes.

### 34. What is method overriding?

Method overriding occurs when a child class provides its own implementation of a method inherited from its parent class.

### 35. Does Python support method overloading?

Python does not support traditional compile-time method overloading by defining multiple methods with the same name and different signatures. Similar behavior can be achieved using default arguments, `*args`, and dispatch techniques.

### 36. Difference between instance, class, and static methods?

- Instance method receives `self`.
- Class method receives `cls` and uses `@classmethod`.
- Static method receives neither automatically and uses `@staticmethod`.

## Python Coding Questions with Answers

### 1. Reverse a string

```python
s = "python"
print(s[::-1])
```

### 2. Check palindrome

```python
s = "madam"
print(s == s[::-1])
```

### 3. Factorial

```python
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)
```

### 4. Fibonacci series

```python
a, b = 0, 1

for _ in range(10):
    print(a, end=" ")
    a, b = b, a + b
```

### 5. Find second-largest distinct element

```python
arr = [10, 20, 30, 20, 40]

unique = sorted(set(arr))

print(unique[-2] if len(unique) >= 2 else None)
```

### 6. Count character frequency

```python
from collections import Counter

s = "programming"
print(Counter(s))
```

### 7. Check anagrams

```python
a = "listen"
b = "silent"

print(sorted(a) == sorted(b))
```

### 8. Find duplicates

```python
arr = [1, 2, 3, 2, 4, 1]

seen = set()
duplicates = set()

for x in arr:
    if x in seen:
        duplicates.add(x)
    seen.add(x)

print(duplicates)
```

### 9. Find missing number from 1 to n

```python
arr = [1, 2, 4, 5]
n = 5

missing = n * (n + 1) // 2 - sum(arr)
print(missing)
```

### 10. Binary search

```python
def binary_search(arr, target):
    low, high = 0, len(arr) - 1

    while low <= high:
        mid = (low + high) // 2

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1

    return -1
```

## Python Learning Resources

- Official Documentation: https://docs.python.org/3/
- Python Tutorial: https://docs.python.org/3/tutorial/
- Programiz: https://www.programiz.com/python-programming
- W3Schools: https://www.w3schools.com/python/
- GeeksforGeeks: https://www.geeksforgeeks.org/python/
- HackerRank: https://www.hackerrank.com/domains/python

---

# 2. Java Interview Questions and Answers

## Java Fundamentals

### 1. What is Java?

Java is a high-level, class-based, object-oriented programming language designed to be portable across platforms using the Java Virtual Machine.

### 2. What are the features of Java?

- Platform independence.
- Object-oriented programming.
- Strong type checking.
- Automatic garbage collection.
- Multithreading support.
- Exception handling.
- Rich standard libraries.

### 3. Why is Java platform-independent?

Java source code is compiled into bytecode. The bytecode can run on any operating system that has a compatible JVM.

### 4. Difference between JDK, JRE, and JVM?

- JDK: Development kit containing tools to develop Java applications.
- JRE: Runtime environment required to run Java applications.
- JVM: Virtual machine that executes Java bytecode.

### 5. What is bytecode?

Bytecode is the intermediate representation generated by the Java compiler. The JVM executes it.

### 6. What are primitive data types?

Java has eight primitive types:

`byte`, `short`, `int`, `long`, `float`, `double`, `char`, and `boolean`.

### 7. Difference between == and equals()?

- `==` compares primitive values or object references.
- `equals()` checks logical equality when properly implemented by a class.

### 8. Difference between String, StringBuilder, and StringBuffer?

- String is immutable.
- StringBuilder is mutable and generally faster for single-threaded modifications.
- StringBuffer is mutable and synchronizes its methods.

### 9. Why are Strings immutable in Java?

Immutability improves security, enables safe sharing, supports string pooling, and makes strings reliable as hash-based collection keys.

### 10. What is the static keyword?

`static` makes a member belong to the class rather than to individual objects.

### 11. What is the final keyword?

- Final variable: Cannot be reassigned.
- Final method: Cannot be overridden.
- Final class: Cannot be extended.

### 12. Difference between final, finally, and finalize()?

- `final`: Keyword used to restrict modification or inheritance.
- `finally`: Exception-handling block.
- `finalize()`: Deprecated finalization mechanism; should not be relied upon for resource cleanup.

### 13. What are access modifiers?

Java provides:

- `public`
- `protected`
- package-private (no modifier)
- `private`

They control visibility and accessibility.

### 14. What is a constructor?

A constructor initializes an object. It has the same name as the class and has no return type.

### 15. What is the this keyword?

`this` refers to the current object.

### 16. What is the super keyword?

`super` refers to the immediate parent class and can access its constructors and members.

## Java OOP

### 17. What are the four pillars of OOP?

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

### 18. What is method overloading?

Multiple methods in the same class have the same name but different parameter lists.

### 19. What is method overriding?

A subclass provides a compatible implementation of an inherited instance method.

### 20. Difference between overloading and overriding?

| Overloading | Overriding |
|---|---|
| Same method name, different parameters | Same compatible method signature |
| Usually within one class | Requires inheritance |
| Resolved at compile time | Uses runtime dispatch for instance methods |

### 21. Does Java support multiple inheritance?

Java does not support multiple inheritance of classes. It supports implementing multiple interfaces.

### 22. Difference between abstract class and interface?

- Abstract classes can have instance state, constructors, and abstract or concrete methods.
- Interfaces define contracts and can also contain default, static, and private methods.
- A class can extend one class but implement multiple interfaces.

### 23. What is encapsulation?

Encapsulation protects an object's internal state by controlling access through methods.

### 24. What is polymorphism?

Polymorphism allows a common interface to represent different implementations. Runtime polymorphism is achieved through method overriding.

## Java Collections and Exception Handling

### 25. What is the Java Collections Framework?

It is a set of interfaces and classes used to store and manipulate groups of objects.

Examples include List, Set, Queue, and Map.

### 26. Difference between ArrayList and LinkedList?

- ArrayList uses a dynamic array and provides fast indexed access.
- LinkedList uses a doubly linked structure and has slower indexed access.
- Insertion or deletion performance depends on the position and whether the relevant node is already available.

### 27. Difference between HashMap and Hashtable?

- HashMap is not synchronized and permits one null key.
- Hashtable is synchronized and does not allow null keys or values.
- ConcurrentHashMap is generally preferred for concurrent access.

### 28. Difference between HashSet and TreeSet?

- HashSet stores unique elements without guaranteed sorted order.
- TreeSet stores unique elements in sorted order.

### 29. Difference between List, Set, and Map?

- List: Ordered collection that allows duplicates.
- Set: Collection of unique elements.
- Map: Stores key-value pairs with unique keys.

### 30. How does HashMap work internally?

HashMap calculates a hash from the key, maps it to a bucket, and stores the key-value entry there. Collisions are handled within the bucket using equality checks and, in suitable cases, tree-based structures.

### 31. What is an exception?

An exception is an event that interrupts the normal execution of a program.

### 32. Difference between checked and unchecked exceptions?

- Checked exceptions are checked by the compiler and must be caught or declared.
- Unchecked exceptions are subclasses of RuntimeException and are not subject to that requirement.

### 33. Difference between throw and throws?

- `throw` explicitly throws an exception.
- `throws` declares exceptions that a method may pass to its caller.

### 34. What is multithreading?

Multithreading allows multiple threads to execute concurrently within a process.

### 35. What is garbage collection?

Garbage collection automatically reclaims memory occupied by objects that are no longer reachable.

## Java Coding Questions with Answers

### 1. Reverse a string

```java
String s = "Java";
String reversed = new StringBuilder(s).reverse().toString();

System.out.println(reversed);
```

### 2. Check palindrome

```java
String s = "madam";
String reversed = new StringBuilder(s).reverse().toString();

System.out.println(s.equals(reversed));
```

### 3. Factorial

```java
int n = 5;
int fact = 1;

for (int i = 1; i <= n; i++) {
    fact *= i;
}

System.out.println(fact);
```

### 4. Fibonacci series

```java
int a = 0, b = 1;

for (int i = 0; i < 10; i++) {
    System.out.print(a + " ");
    int c = a + b;
    a = b;
    b = c;
}
```

### 5. Find the second-largest distinct element

```java
int[] arr = {10, 20, 30, 20, 40};

int largest = Integer.MIN_VALUE;
int second = Integer.MIN_VALUE;

for (int x : arr) {
    if (x > largest) {
        second = largest;
        largest = x;
    } else if (x > second && x != largest) {
        second = x;
    }
}

System.out.println(second);
```

### 6. Check prime number

```java
int n = 29;
boolean prime = n >= 2;

for (int i = 2; i * i <= n; i++) {
    if (n % i == 0) {
        prime = false;
        break;
    }
}

System.out.println(prime);
```

### 7. Find character frequency

```java
String s = "programming";

Map<Character, Integer> map = new HashMap<>();

for (char c : s.toCharArray()) {
    map.put(c, map.getOrDefault(c, 0) + 1);
}

System.out.println(map);
```

### 8. Binary search

```java
static int binarySearch(int[] arr, int target) {
    int low = 0, high = arr.length - 1;

    while (low <= high) {
        int mid = low + (high - low) / 2;

        if (arr[mid] == target)
            return mid;
        else if (arr[mid] < target)
            low = mid + 1;
        else
            high = mid - 1;
    }

    return -1;
}
```

## Java Learning Resources

- Official Java Learning: https://dev.java/learn/
- Java Documentation: https://docs.oracle.com/en/java/
- Programiz: https://www.programiz.com/java-programming
- W3Schools: https://www.w3schools.com/java/
- GeeksforGeeks: https://www.geeksforgeeks.org/java/
- HackerRank: https://www.hackerrank.com/domains/java

---

# 3. SQL Interview Questions and Solved Queries

## SQL Fundamentals

### 1. What is SQL?

SQL stands for Structured Query Language. It is used to create, retrieve, update, and manage data in relational databases.

### 2. Difference between SQL and MySQL?

SQL is a query language. MySQL is a relational database management system that uses SQL.

### 3. What are DDL, DML, DQL, DCL, and TCL?

- DDL: Data Definition Language – CREATE, ALTER, DROP, TRUNCATE.
- DML: Data Manipulation Language – INSERT, UPDATE, DELETE.
- DQL: Data Query Language – SELECT.
- DCL: Data Control Language – GRANT, REVOKE.
- TCL: Transaction Control Language – COMMIT, ROLLBACK, SAVEPOINT.

### 4. Difference between DELETE, DROP, and TRUNCATE?

| DELETE | DROP | TRUNCATE |
|---|---|---|
| Removes selected rows or all rows | Removes the table itself | Removes all table rows |
| Supports WHERE | No WHERE | No WHERE |
| Table structure remains | Table structure is removed | Table structure remains |

Transaction and rollback behavior can vary by database system.

### 5. Difference between WHERE and HAVING?

- WHERE filters individual rows before grouping.
- HAVING filters groups after GROUP BY.

```sql
SELECT dept_id, COUNT(*)
FROM Employee
WHERE salary > 30000
GROUP BY dept_id
HAVING COUNT(*) > 2;
```

### 6. Difference between GROUP BY and ORDER BY?

- GROUP BY combines rows into groups for aggregation.
- ORDER BY sorts the resulting rows.

### 7. What is a primary key?

A primary key uniquely identifies each row in a table. It cannot contain NULL values.

### 8. What is a foreign key?

A foreign key references a candidate or primary key in another table and helps maintain referential integrity.

### 9. What is a unique constraint?

A unique constraint ensures that values in a column or combination of columns are unique. NULL handling varies by database.

### 10. What is NULL?

NULL represents missing or unknown data. It must be checked using `IS NULL` or `IS NOT NULL`, not `= NULL`.

### 11. Difference between CHAR and VARCHAR?

- CHAR uses fixed-length storage semantics.
- VARCHAR stores variable-length strings.

### 12. Difference between COUNT(*) and COUNT(column)?

- COUNT(*) counts rows.
- COUNT(column) counts non-NULL values in that column.
- COUNT(DISTINCT column) counts distinct non-NULL values.

### 13. What is a subquery?

A subquery is a query nested inside another SQL query.

### 14. What is a correlated subquery?

A correlated subquery refers to columns from the outer query and is logically evaluated in relation to each outer row.

### 15. What is a view?

A view is a virtual table defined by a SQL query. It usually stores the query definition rather than a separate copy of the underlying data.

### 16. What is an index?

An index is a data structure that helps the database find rows faster. It can improve reads but requires storage and can add overhead to inserts, updates, and deletes.

### 17. What is a stored procedure?

A stored procedure is a named collection of SQL statements stored in the database and executed when called.

### 18. What is a trigger?

A trigger is database code that executes automatically in response to specified events such as INSERT, UPDATE, or DELETE.

## SQL Practice Tables

Assume these tables:

**Employee**

| emp_id | emp_name | salary | dept_id | manager_id |
|---|---|---:|---:|---:|
| 1 | Arun | 50000 | 10 | NULL |
| 2 | Ravi | 60000 | 20 | 1 |
| 3 | Priya | 70000 | 10 | 1 |
| 4 | Kiran | 45000 | 30 | 2 |
| 5 | Sita | 80000 | 20 | 2 |

**Department**

| dept_id | dept_name |
|---|---|
| 10 | IT |
| 20 | HR |
| 30 | Finance |

## Basic SQL Queries

### 1. Display all employees.

```sql
SELECT * FROM Employee;
```

### 2. Find employees earning more than 50000.

```sql
SELECT *
FROM Employee
WHERE salary > 50000;
```

### 3. Display employees in descending order of salary.

```sql
SELECT *
FROM Employee
ORDER BY salary DESC;
```

### 4. Find the total number of employees.

```sql
SELECT COUNT(*)
FROM Employee;
```

### 5. Find the average salary.

```sql
SELECT AVG(salary)
FROM Employee;
```

### 6. Find the maximum and minimum salary.

```sql
SELECT MAX(salary), MIN(salary)
FROM Employee;
```

### 7. Find employees whose names start with A.

```sql
SELECT *
FROM Employee
WHERE emp_name LIKE 'A%';
```

### 8. Find employees earning between 40000 and 70000.

```sql
SELECT *
FROM Employee
WHERE salary BETWEEN 40000 AND 70000;
```

### 9. Find employees without managers.

```sql
SELECT *
FROM Employee
WHERE manager_id IS NULL;
```

### 10. Find employees in departments 10 and 20.

```sql
SELECT *
FROM Employee
WHERE dept_id IN (10, 20);
```

## Intermediate SQL Queries

### 11. Find the second-highest salary.

```sql
SELECT MAX(salary)
FROM Employee
WHERE salary < (
    SELECT MAX(salary)
    FROM Employee
);
```

### 12. Find the third-highest distinct salary.

```sql
SELECT DISTINCT salary
FROM Employee
ORDER BY salary DESC
LIMIT 1 OFFSET 2;
```

### 13. Find the number of employees in each department.

```sql
SELECT dept_id, COUNT(*) AS employee_count
FROM Employee
GROUP BY dept_id;
```

### 14. Find departments having more than one employee.

```sql
SELECT dept_id, COUNT(*) AS employee_count
FROM Employee
GROUP BY dept_id
HAVING COUNT(*) > 1;
```

### 15. Display employee names with department names.

```sql
SELECT e.emp_name, d.dept_name
FROM Employee e
INNER JOIN Department d
ON e.dept_id = d.dept_id;
```

### 16. Display all employees, even if their department does not match.

```sql
SELECT e.emp_name, d.dept_name
FROM Employee e
LEFT JOIN Department d
ON e.dept_id = d.dept_id;
```

### 17. Find employees earning more than the average salary.

```sql
SELECT *
FROM Employee
WHERE salary > (
    SELECT AVG(salary)
    FROM Employee
);
```

### 18. Find employees earning more than their department's average salary.

```sql
SELECT e.*
FROM Employee e
WHERE e.salary > (
    SELECT AVG(e2.salary)
    FROM Employee e2
    WHERE e2.dept_id = e.dept_id
);
```

### 19. Display employee names and manager names.

```sql
SELECT e.emp_name AS employee,
       m.emp_name AS manager
FROM Employee e
LEFT JOIN Employee m
ON e.manager_id = m.emp_id;
```

### 20. Find departments that have no employees.

```sql
SELECT d.*
FROM Department d
LEFT JOIN Employee e
ON d.dept_id = e.dept_id
WHERE e.emp_id IS NULL;
```

## Advanced SQL Queries

### 21. Find duplicate employee names.

```sql
SELECT emp_name, COUNT(*)
FROM Employee
GROUP BY emp_name
HAVING COUNT(*) > 1;
```

### 22. Find employees with the highest salary in each department.

```sql
SELECT *
FROM Employee e
WHERE salary = (
    SELECT MAX(e2.salary)
    FROM Employee e2
    WHERE e2.dept_id = e.dept_id
);
```

### 23. Find the top three salaries in each department.

```sql
SELECT *
FROM (
    SELECT e.*,
           DENSE_RANK() OVER (
               PARTITION BY dept_id
               ORDER BY salary DESC
           ) AS salary_rank
    FROM Employee e
) ranked
WHERE salary_rank <= 3;
```

### 24. Find employees who earn more than their managers.

```sql
SELECT e.emp_name, e.salary,
       m.emp_name AS manager, m.salary AS manager_salary
FROM Employee e
JOIN Employee m
ON e.manager_id = m.emp_id
WHERE e.salary > m.salary;
```

### 25. Rank employees based on salary.

```sql
SELECT emp_name, salary,
       RANK() OVER (ORDER BY salary DESC) AS salary_rank
FROM Employee;
```

### 26. Find the running total of salaries.

```sql
SELECT emp_id, emp_name, salary,
       SUM(salary) OVER (
           ORDER BY emp_id
       ) AS running_total
FROM Employee;
```

### 27. Find the difference between maximum and minimum salaries.

```sql
SELECT MAX(salary) - MIN(salary) AS salary_difference
FROM Employee;
```

### 28. Find employees having the same salary.

```sql
SELECT *
FROM Employee
WHERE salary IN (
    SELECT salary
    FROM Employee
    GROUP BY salary
    HAVING COUNT(*) > 1
);
```

### 29. Find the percentage contribution of each department to total salary.

```sql
SELECT dept_id,
       SUM(salary) AS department_salary,
       ROUND(
           SUM(salary) * 100.0 /
           (SELECT SUM(salary) FROM Employee),
           2
       ) AS percentage
FROM Employee
GROUP BY dept_id;
```

### 30. Find the Nth-highest distinct salary without LIMIT.

```sql
SELECT salary
FROM (
    SELECT DISTINCT salary,
           DENSE_RANK() OVER (
               ORDER BY salary DESC
           ) AS r
    FROM Employee
) ranked
WHERE r = 3;
```

This example finds the third-highest distinct salary.

## SQL JOIN Types

| Join | Meaning |
|---|---|
| INNER JOIN | Returns matching rows from both tables |
| LEFT JOIN | Returns all left-table rows and matching right-table rows |
| RIGHT JOIN | Returns all right-table rows and matching left-table rows |
| FULL OUTER JOIN | Returns matched and unmatched rows from both sides |
| CROSS JOIN | Returns Cartesian product |
| SELF JOIN | Joins a table with itself |

## SQL Resources

- SQLBolt: https://sqlbolt.com/
- SQLZoo: https://sqlzoo.net/wiki/SQL_Tutorial
- HackerRank SQL: https://www.hackerrank.com/domains/sql
- LeetCode Database: https://leetcode.com/problemset/database/
- MySQL Documentation: https://dev.mysql.com/doc/
- W3Schools SQL: https://www.w3schools.com/sql/
- Mode SQL Tutorial: https://mode.com/sql-tutorial/

---

# 4. DBMS Interview Questions and Answers

## DBMS Fundamentals

### 1. What is DBMS?

A Database Management System is software used to store, organize, retrieve, and manage data efficiently.

Examples: MySQL, Oracle Database, PostgreSQL, SQL Server.

### 2. What is RDBMS?

A Relational Database Management System stores data in related tables consisting of rows and columns.

### 3. Difference between DBMS and RDBMS?

- DBMS is a general system for managing databases.
- RDBMS organizes data using relations (tables) and supports relational constraints.
- RDBMS commonly supports keys and relationships between tables.

### 4. What are the advantages of DBMS?

- Reduces unnecessary data duplication.
- Supports data consistency.
- Provides access control.
- Supports backup and recovery.
- Allows concurrent access.
- Provides structured data management.

### 5. What is a database schema?

A schema defines the logical structure of a database, including tables, columns, relationships, and constraints.

### 6. What is a database instance?

An instance is the actual data stored in the database at a particular point in time.

### 7. What is a primary key?

A primary key uniquely identifies each record in a table. It must be unique and non-NULL.

### 8. What is a candidate key?

A candidate key is a minimal set of attributes that uniquely identifies a record.

### 9. What is a super key?

A super key is any set of one or more attributes that uniquely identifies a record. It may contain extra attributes.

### 10. What is a composite key?

A composite key consists of two or more columns used together to uniquely identify a record.

### 11. What is a foreign key?

A foreign key is a column or group of columns that references a candidate key, usually the primary key, in another table.

### 12. What is referential integrity?

Referential integrity ensures that foreign key references remain valid according to the database constraints.

### 13. What is data redundancy?

Data redundancy means storing the same information unnecessarily in multiple places.

### 14. What is data inconsistency?

Data inconsistency occurs when different copies of the same information contain conflicting values.

## Database Normalization

### 15. What is normalization?

Normalization organizes database tables to reduce redundancy and prevent insertion, deletion, and update anomalies.

### 16. What is 1NF?

First Normal Form requires each column to contain atomic values and each row to be uniquely identifiable.

### 17. What is 2NF?

Second Normal Form requires the table to be in 1NF and every non-prime attribute to be fully dependent on every candidate key, meaning no partial dependency on a proper subset of a candidate key.

### 18. What is 3NF?

Third Normal Form requires the table to be in 2NF and non-prime attributes must not have transitive dependencies on candidate keys. Formally, for every non-trivial functional dependency X → A, X must be a super key or A must be a prime attribute.

### 19. What is BCNF?

Boyce-Codd Normal Form requires every determinant of a non-trivial
