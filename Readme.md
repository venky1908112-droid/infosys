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

Boyce-Codd Normal Form requires every determinant of a non-trivial functional dependency to be a super key.

### 20. Difference between 3NF and BCNF?

BCNF is stricter than 3NF. In BCNF, every determinant must be a super key, while 3NF permits certain dependencies where the dependent attribute is prime.

### 21. What is a functional dependency?

A functional dependency X → Y means that each value of X determines exactly one value of Y.

### 22. What is a partial dependency?

A partial dependency occurs when a non-prime attribute depends on only part of a composite candidate key.

### 23. What is a transitive dependency?

A transitive dependency occurs when an attribute depends on a key through another non-key attribute.

### 24. What is denormalization?

Denormalization intentionally introduces some redundancy to improve query performance or simplify reads.

## Transactions and ACID Properties

### 25. What is a transaction?

A transaction is a logical unit of database operations that should be completed as a single reliable operation.

Example: Transferring money from one bank account to another.

### 26. Explain ACID properties.

- Atomicity: All operations happen or none happen.
- Consistency: A transaction preserves database rules.
- Isolation: Concurrent transactions should not interfere in prohibited ways.
- Durability: Committed changes survive failures according to the database's guarantees.

### 27. What is COMMIT?

COMMIT permanently saves the changes made by a transaction.

### 28. What is ROLLBACK?

ROLLBACK undoes uncommitted changes in the current transaction.

### 29. What is SAVEPOINT?

SAVEPOINT creates a point within a transaction to which a partial rollback can be performed.

### 30. What are transaction states?

Common states include Active, Partially Committed, Committed, Failed, and Aborted.

## Indexing and Concurrency

### 31. What is indexing?

Indexing creates an auxiliary data structure to speed up data retrieval.

### 32. What are the disadvantages of indexing?

- Requires additional storage.
- Can slow down INSERT, UPDATE, and DELETE.
- Requires maintenance.

### 33. What is a B-tree?

A B-tree is a balanced search tree designed for efficient searching, insertion, and deletion.

### 34. What is a B+ tree?

A B+ tree stores actual data entries or record pointers at leaf nodes, while internal nodes guide the search. Linked leaves make range scans efficient.

### 35. What is a deadlock?

A deadlock occurs when two or more transactions wait indefinitely for resources held by one another.

### 36. What is concurrency control?

Concurrency control manages simultaneous transactions to maintain database correctness and isolation.

### 37. What is locking?

Locking controls access to database resources while transactions execute.

### 38. Difference between shared and exclusive locks?

- Shared lock permits multiple transactions to read a resource.
- Exclusive lock permits a transaction to modify a resource and generally prevents other conflicting access.

### 39. What is two-phase locking?

Two-phase locking has two phases:

1. Growing phase: Locks are acquired and not released.
2. Shrinking phase: Locks are released and no new locks are acquired.

It helps ensure conflict serializability.

### 40. What is serializability?

Serializability means concurrent transactions produce a result equivalent to some serial execution order.

### 41. What is a dirty read?

A dirty read occurs when a transaction reads uncommitted data written by another transaction.

### 42. What is a non-repeatable read?

A transaction reads the same row twice and gets different values because another transaction committed an update between the reads.

### 43. What is a phantom read?

A transaction repeats a range query and sees additional or missing rows because another transaction inserted or deleted matching rows.

### 44. What are isolation levels?

Common SQL isolation levels are:

- Read Uncommitted
- Read Committed
- Repeatable Read
- Serializable

Exact behavior can vary between database engines.

## DBMS Resources

- GeeksforGeeks: https://www.geeksforgeeks.org/dbms/
- TutorialsPoint: https://www.tutorialspoint.com/dbms/
- PostgreSQL: https://www.postgresql.org/docs/
- Oracle Database Concepts: https://docs.oracle.com/en/database/oracle/oracle-database/
- Gate Smashers: https://www.youtube.com/@GateSmashers

---

# 5. Computer Networks Interview Questions and Answers

## Network Fundamentals

### 1. What is a computer network?

A computer network is a collection of interconnected devices that communicate and share resources.

### 2. What are LAN, MAN, and WAN?

- LAN: Local Area Network, covering a small area.
- MAN: Metropolitan Area Network, covering a city or metropolitan region.
- WAN: Wide Area Network, covering large geographical areas.

### 3. What is an IP address?

An IP address is a logical address used to identify a device or interface on an IP network.

### 4. Difference between IPv4 and IPv6?

- IPv4 uses 32-bit addresses.
- IPv6 uses 128-bit addresses.
- IPv6 provides a much larger address space and has a different packet format.

### 5. What is a MAC address?

A MAC address is a link-layer hardware address used for communication on a local network. It is typically assigned to a network interface.

### 6. Difference between IP and MAC address?

- IP address is used for logical addressing and routing between networks.
- MAC address is used for local link-layer delivery.
- IP addresses can change depending on the network; MAC addresses are generally assigned to interfaces.

### 7. What is a port number?

A port number identifies a communication endpoint associated with a process or service on a device.

Examples:
- HTTP: 80
- HTTPS: 443
- SSH: 22
- DNS: 53
- FTP control: 21

### 8. What is bandwidth?

Bandwidth is the maximum data-transfer capacity of a communication link, usually measured in bits per second.

### 9. What is latency?

Latency is the time taken for data to travel from one point to another.

### 10. What is packet switching?

Packet switching divides data into packets that are transmitted independently through a network and reassembled at the destination.

### 11. What is DNS?

Domain Name System translates domain names such as `example.com` into IP addresses and other DNS records.

### 12. What is DHCP?

Dynamic Host Configuration Protocol automatically provides network configuration such as IP address, subnet mask, gateway, and DNS servers.

### 13. What is a gateway?

A gateway connects different networks. A default gateway is typically the router used to reach destinations outside the local network.

## OSI and TCP/IP Models

### 14. What is the OSI model?

The Open Systems Interconnection model is a seven-layer conceptual framework used to understand network communication.

### 15. Explain the seven OSI layers.

1. Physical: Transmits raw bits.
2. Data Link: Handles frames and local delivery.
3. Network: Handles logical addressing and routing.
4. Transport: Provides end-to-end transport.
5. Session: Manages communication sessions.
6. Presentation: Handles data representation, encoding, and related functions.
7. Application: Provides network services to applications.

### 16. What is the TCP/IP model?

The TCP/IP model describes Internet communication using layers commonly represented as:

1. Application
2. Transport
3. Internet
4. Network Access or Link

### 17. Difference between OSI and TCP/IP?

OSI is a seven-layer reference model. TCP/IP is a practical networking architecture used by the Internet and is commonly represented using four layers.

### 18. Which layer is responsible for routing?

The Network layer in OSI, corresponding to the Internet layer in TCP/IP.

### 19. Which layer handles encryption?

Encryption can be implemented at different layers. TLS is commonly associated with the application-facing transport security stack, while encryption can also occur at lower layers.

### 20. What is encapsulation?

Encapsulation is the process of adding protocol headers, and sometimes trailers, as data moves down the network stack.

## TCP and UDP

### 21. What is TCP?

Transmission Control Protocol is a connection-oriented transport protocol that provides reliable, ordered byte-stream delivery.

### 22. What is UDP?

User Datagram Protocol is a connectionless transport protocol that sends datagrams without guaranteeing delivery, order, or duplicate protection.

### 23. Difference between TCP and UDP?

| TCP | UDP |
|---|---|
| Connection-oriented | Connectionless |
| Reliable delivery | No delivery guarantee |
| Ordered byte stream | Independent datagrams |
| More transport overhead | Lower overhead |
| Used for many web and file-transfer connections | Used in DNS, real-time media, and other applications |

### 24. What is the TCP three-way handshake?

TCP establishes a connection using:

1. SYN: Client requests connection.
2. SYN-ACK: Server acknowledges and responds.
3. ACK: Client acknowledges the response.

### 25. What is TCP four-way termination?

A typical graceful TCP close involves:

1. FIN from one side.
2. ACK from the other side.
3. FIN from the other side.
4. ACK from the first side.

### 26. What is flow control?

Flow control prevents a sender from overwhelming the receiver. TCP uses a receive window to communicate how much data the receiver can accept.

### 27. What is congestion control?

Congestion control manages the amount of data sent into the network to reduce congestion and packet loss.

### 28. What is a socket?

A socket is a communication endpoint identified by an IP address, transport protocol, and port.

## Important Networking Concepts

### 29. What is HTTP?

Hypertext Transfer Protocol is an application-layer protocol used for communication between web clients and servers.

### 30. What is HTTPS?

HTTPS is HTTP protected by TLS, providing encryption, integrity protection, and server authentication.

### 31. Difference between HTTP and HTTPS?

HTTP does not itself provide TLS security. HTTPS uses TLS to protect the communication channel.

### 32. What is SSL/TLS?

TLS is a cryptographic protocol that provides secure communication. SSL is its older predecessor and is deprecated.

### 33. What is a firewall?

A firewall monitors and controls network traffic according to security rules.

### 34. What is a proxy server?

A proxy acts as an intermediary between a client and another server.

### 35. What is a VPN?

A Virtual Private Network creates a protected connection across another network, often using encryption and tunneling.

### 36. What is NAT?

Network Address Translation modifies IP address information in packet headers, commonly allowing multiple private devices to share a public IP address.

### 37. What is a subnet mask?

A subnet mask identifies which part of an IPv4 address represents the network and which part represents the host.

### 38. What is ARP?

Address Resolution Protocol maps an IPv4 address to a link-layer address on a local network.

### 39. What is ICMP?

Internet Control Message Protocol is used for network diagnostics and error reporting. Tools such as ping commonly use ICMP Echo messages.

### 40. Difference between hub, switch, and router?

- Hub: Broadcasts incoming signals to all ports.
- Switch: Forwards frames based on MAC addresses.
- Router: Forwards packets between networks using IP addresses.

### 41. What happens when you enter a URL in a browser?

A simplified sequence:

1. Browser parses the URL.
2. Browser checks relevant caches.
3. DNS resolves the domain name.
4. The browser establishes a connection with the server.
5. TLS negotiation occurs for HTTPS.
6. Browser sends an HTTP request.
7. Server processes the request and responds.
8. Browser processes the response and renders the page.

### 42. What are HTTP status codes?

- 1xx: Informational.
- 2xx: Success.
- 3xx: Redirection.
- 4xx: Client error.
- 5xx: Server error.

Common examples:
- 200: OK
- 201: Created
- 301: Moved Permanently
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Internal Server Error
- 503: Service Unavailable

## Computer Networks Resources

- Cloudflare Learning Center: https://www.cloudflare.com/learning/
- Cisco Networking Academy: https://www.netacad.com/
- GeeksforGeeks: https://www.geeksforgeeks.org/computer-network-tutorials/
- Kurose and Ross Companion Website: https://gaia.cs.umass.edu/kurose_ross/
- Gate Smashers: https://www.youtube.com/@GateSmashers

---

# 6. Operating Systems Interview Questions and Answers

## Operating System Fundamentals

### 1. What is an operating system?

An operating system is system software that manages computer hardware, software resources, processes, memory, files, and input/output devices.

Examples: Windows, Linux, macOS, Android.

### 2. What are the main functions of an operating system?

- Process management.
- Memory management.
- File management.
- Device management.
- Security and access control.
- Resource allocation.
- User interface.

### 3. What are the types of operating systems?

- Batch operating systems.
- Time-sharing operating systems.
- Distributed operating systems.
- Real-time operating systems.
- Network operating systems.
- Multiprocessing operating systems.

### 4. What is a kernel?

The kernel is the core component of an operating system. It manages hardware resources and provides essential services to processes.

### 5. What is a system call?

A system call is a mechanism through which a user program requests a service from the operating system kernel.

Examples include file operations, process creation, and memory management.

### 6. Difference between kernel and shell?

- Kernel manages system resources and hardware.
- Shell provides an interface through which users interact with the operating system.

### 7. What is booting?

Booting is the process of starting a computer and loading the operating system into memory.

### 8. What is multitasking?

Multitasking allows multiple tasks to make progress through CPU scheduling and resource sharing.

### 9. What is multiprocessing?

Multiprocessing uses multiple CPUs or CPU cores to execute processes in parallel.

### 10. What is multithreading?

Multithreading allows multiple threads within a process to execute concurrently.

## Process Management

### 11. What is a process?

A process is a program in execution, including its execution state and allocated resources.

### 12. What is a thread?

A thread is the smallest unit of execution scheduled by the operating system. Threads in the same process share much of the process's resources.

### 13. Difference between process and thread?

| Process | Thread |
|---|---|
| Independent execution unit | Execution unit within a process |
| Separate address space | Shares process address space |
| Higher resource overhead | Generally lower overhead |
| Communication often requires IPC | Communication can use shared memory |

### 14. What are the states of a process?

Common process states are:

1. New
2. Ready
3. Running
4. Waiting or Blocked
5. Terminated

### 15. What is PCB?

Process Control Block is a data structure maintained by the operating system to store process information such as process ID, state, registers, scheduling information, and memory information.

### 16. What is context switching?

Context switching is the process of saving the state of one execution context and restoring another so the CPU can switch between processes or threads.

### 17. What is Inter-Process Communication?

IPC allows processes to exchange information and coordinate their execution.

Examples:
- Pipes.
- Message queues.
- Shared memory.
- Sockets.
- Signals.

### 18. What is process scheduling?

Process scheduling determines which ready process should execute on the CPU.

### 19. Difference between preemptive and non-preemptive scheduling?

- Preemptive scheduling allows the OS to interrupt a running process.
- Non-preemptive scheduling generally lets a process continue until it blocks, finishes, or voluntarily yields.

## CPU Scheduling Algorithms

### 20. What is FCFS?

First Come First Serve executes processes in the order they arrive. It is simple but can cause the convoy effect.

### 21. What is SJF?

Shortest Job First selects the available process with the smallest expected CPU burst. It can minimize average waiting time under ideal assumptions.

### 22. What is SRTF?

Shortest Remaining Time First is the preemptive version of SJF. It selects the process with the shortest remaining CPU burst.

### 23. What is Round Robin?

Round Robin assigns each process a fixed time quantum. If a process does not finish within the quantum, it is moved to the back of the ready queue.

### 24. What is Priority Scheduling?

Priority Scheduling selects the process with the highest priority. Low-priority processes may suffer starvation.

### 25. What is starvation?

Starvation occurs when a process waits indefinitely because resources or CPU time keep being allocated to other processes.

### 26. What is aging?

Aging gradually increases the priority of waiting processes to prevent starvation.

### 27. What are turnaround time and waiting time?

- Turnaround Time = Completion Time − Arrival Time.
- Waiting Time = Turnaround Time − CPU Burst Time, for the basic single-burst scheduling model.

### 28. What is response time?

Response Time = First CPU Start Time − Arrival Time.

## Deadlocks and Synchronization

### 29. What is a deadlock?

A deadlock occurs when a group of processes waits indefinitely for resources held by one another.

### 30. What are the four necessary conditions for deadlock?

1. Mutual Exclusion.
2. Hold and Wait.
3. No Preemption.
4. Circular Wait.

All four must hold simultaneously for a deadlock to occur under the classic model.

### 31. What is deadlock prevention?

Deadlock prevention ensures at least one necessary deadlock condition cannot hold.

### 32. What is deadlock avoidance?

Deadlock avoidance checks whether resource allocation will keep the system in a safe state before granting requests.

### 33. What is Banker's Algorithm?

Banker's Algorithm is a deadlock-avoidance algorithm that checks whether granting a resource request leaves the system in a safe state.

### 34. What is a semaphore?

A semaphore is a synchronization mechanism that uses an integer counter and atomic operations such as wait and signal to coordinate access to resources.

### 35. What is a mutex?

A mutex is a mutual-exclusion lock that allows only one thread at a time to enter a protected critical section.

### 36. Difference between mutex and semaphore?

- Mutex is generally used for exclusive ownership of a resource.
- Semaphore manages permits or resource availability and can allow multiple concurrent users depending on its count.

### 37. What is a critical section?

A critical section is a part of code that accesses shared data or resources and must be protected against unsafe concurrent execution.

### 38. What is a race condition?

A race condition occurs when program correctness depends on the timing or ordering of concurrent operations.

### 39. What is the producer-consumer problem?

It is a synchronization problem where producers add items to a shared buffer and consumers remove them. Synchronization is needed to prevent overflow, underflow, and race conditions.

### 40. What is the dining philosophers problem?

It is a classic synchronization problem illustrating deadlock and resource contention when several processes compete for limited shared resources.

## Memory Management

### 41. What is memory management?

Memory management is the OS function responsible for allocating, tracking, protecting, and reclaiming memory.

### 42. What is paging?

Paging divides virtual memory into fixed-size pages and physical memory into fixed-size frames. Pages can be mapped to frames.

### 43. What is segmentation?

Segmentation divides memory into logical variable-sized segments such as code, data, and stack.

### 44. Difference between paging and segmentation?

| Paging | Segmentation |
|---|---|
| Fixed-size blocks | Variable-size blocks |
| Pages and frames | Logical segments |
| Avoids external fragmentation in physical allocation | Can suffer external fragmentation |
| Mostly transparent to programmer | Reflects logical program divisions |

### 45. What is virtual memory?

Virtual memory gives processes the abstraction of a large private address space, with the OS and hardware mapping virtual addresses to physical memory or other backing storage.

### 46. What is demand paging?

Demand paging loads a page into physical memory only when it is needed.

### 47. What is a page fault?

A page fault occurs when a process accesses a virtual page that is not currently mapped to an available physical frame in the required way. The OS handles the fault.

### 48. What is thrashing?

Thrashing occurs when the system spends excessive time handling page faults and swapping pages rather than executing useful work.

### 49. What is fragmentation?

Fragmentation is wasted memory space caused by the way memory is allocated and freed.

### 50. Difference between internal and external fragmentation?

- Internal fragmentation: Unused space inside an allocated block.
- External fragmentation: Free memory exists but is scattered into small non-contiguous blocks.

### 51. What is a page replacement algorithm?

A page replacement algorithm decides which page to remove when a new page must be loaded and no free frame is available.

### 52. Explain FIFO page replacement.

FIFO removes the page that has been in memory the longest.

### 53. Explain LRU page replacement.

Least Recently Used replaces the page that has not been accessed for the longest time.

### 54. Explain Optimal page replacement.

Optimal replaces the page whose next use is farthest in the future. It is mainly a theoretical benchmark because future references are not generally known.

## Operating Systems Resources

- Operating System Concepts: https://www.os-book.com/
- GeeksforGeeks OS: https://www.geeksforgeeks.org/operating-systems/
- TutorialsPoint: https://www.tutorialspoint.com/operating_system/
- Linux Kernel Documentation: https://docs.kernel.org/
- Gate Smashers: https://www.youtube.com/@GateSmashers

---

# 7. Data Structures and Algorithms

For DSE preparation, focus on problem-solving, explaining your approach, and analyzing time and space complexity.

## Important Topics

1. Arrays and Strings
2. Hashing
3. Two Pointers
4. Sliding Window
5. Sorting
6. Binary Search
7. Linked Lists
8. Stacks and Queues
9. Recursion and Backtracking
10. Trees and Binary Search Trees
11. Graphs: BFS and DFS
12. Greedy Algorithms
13. Dynamic Programming
14. Heaps and Priority Queues
15. Bit Manipulation

## Important LeetCode Problems

| Problem | Link |
|---|---|
| Two Sum | https://leetcode.com/problems/two-sum/ |
| Best Time to Buy and Sell Stock | https://leetcode.com/problems/best-time-to-buy-and-sell-stock/ |
| Maximum Subarray | https://leetcode.com/problems/maximum-subarray/ |
| Product of Array Except Self | https://leetcode.com/problems/product-of-array-except-self/ |
| Longest Substring Without Repeating Characters | https://leetcode.com/problems/longest-substring-without-repeating-characters/ |
| Longest Repeating Character Replacement | https://leetcode.com/problems/longest-repeating-character-replacement/ |
| Search in Rotated Sorted Array | https://leetcode.com/problems/search-in-rotated-sorted-array/ |
| Reverse Linked List | https://leetcode.com/problems/reverse-linked-list/ |
| Linked List Cycle | https://leetcode.com/problems/linked-list-cycle/ |
| Valid Parentheses | https://leetcode.com/problems/valid-parentheses/ |
| Binary Tree Level Order Traversal | https://leetcode.com/problems/binary-tree-level-order-traversal/ |
| Maximum Depth of Binary Tree | https://leetcode.com/problems/maximum-depth-of-binary-tree/ |
| Number of Islands | https://leetcode.com/problems/number-of-islands/ |
| Clone Graph | https://leetcode.com/problems/clone-graph/ |
| Jump Game | https://leetcode.com/problems/jump-game/ |
| Coin Change | https://leetcode.com/problems/coin-change/ |
| Longest Increasing Subsequence | https://leetcode.com/problems/longest-increasing-subsequence/ |
| Subsets | https://leetcode.com/problems/subsets/ |
| Combination Sum | https://leetcode.com/problems/combination-sum/ |

## DSA Resources

- LeetCode: https://leetcode.com/
- GeeksforGeeks: https://www.geeksforgeeks.org/
- HackerRank: https://www.hackerrank.com/
- NeetCode Roadmap: https://neetcode.io/roadmap
- Striver A2Z DSA Sheet: https://takeuforward.org/strivers-a2z-dsa-course/strivers-a2z-dsa-course-sheet-2/

---

# 8. Project and Resume-Based Interview Questions

### 1. Explain your project.

Start with the problem statement, explain the solution, describe the technology stack, and summarize your individual contribution.

### 2. Why did you choose this project?

Explain the real-world problem and why your solution is useful.

### 3. Explain your project architecture.

Describe how the frontend communicates with the backend, how the backend processes requests, and how data is stored in the database.

### 4. What was your individual contribution?

Clearly explain the modules you personally designed, implemented, tested, and integrated.

### 5. What was the most challenging part?

Choose a genuine technical challenge and explain the problem, your debugging process, and the solution.

### 6. Why did you choose this technology stack?

Explain the strengths of the technologies and why they fit your requirements.

### 7. How did you implement authentication?

Explain the actual authentication flow, password hashing, session or token management, and authorization checks used in your project.

### 8. How would you scale your project?

Possible improvements include:

- Database indexing.
- Caching.
- Load balancing.
- Horizontal scaling.
- Asynchronous processing.
- Optimized API endpoints.
- Monitoring and logging.

### 9. How did you test your project?

Explain unit testing, integration testing, validation testing, and manual testing actually performed.

### 10. What would you improve?

Mention realistic improvements such as better security, improved performance, responsive UI, stronger validation, and additional features.

## Web Development Questions

### What is Flask?

Flask is a lightweight Python web framework used to build web applications and APIs.

### What is REST?

REST is an architectural style for designing networked applications. REST APIs commonly use HTTP methods and resource-oriented URLs.

### Difference between GET and POST?

- GET requests retrieve data.
- POST requests submit data or request resource creation or processing.

### What is JSON?

JSON is a lightweight text format used to represent structured data.

### What is authentication?

Authentication verifies the identity of a user.

### What is authorization?

Authorization determines what an authenticated user is permitted to access.

### What is CORS?

Cross-Origin Resource Sharing is a browser security mechanism that controls whether a web page can make requests to a different origin.

### What is MVC?

Model-View-Controller is an architectural pattern that separates data and business logic, user interface, and request handling or control flow.

---

# 9. HR and Managerial Interview Questions with Sample Answers

*Adapt these sample answers to your actual experience. Do not memorize them word for word.*

### 1. Tell me about yourself.

**Sample answer:**

"I am a final-year B.Tech Information Technology student. I am interested in software development and problem-solving. I have been practicing data structures and algorithms and have worked on projects involving Python, Flask, MySQL, and web technologies. I enjoy learning new technologies and applying them to practical problems. I am looking forward to starting my career in a role where I can contribute technically and continue learning."

### 2. Why do you want to join Infosys?

**Sample answer:**

"Infosys is a well-established IT services and consulting company with opportunities to work on different technologies and business problems. I am interested in starting my career in an environment where I can learn from experienced professionals, work on real-world projects, and improve my technical and professional skills."

### 3. Why are you interested in the DSE role?

**Sample answer:**

"I am interested in the DSE role because it aligns with my interest in programming, problem-solving, and software development. I want to work on challenging technical problems and develop solutions that have practical business value."

### 4. What are your strengths?

**Sample answer:**

"My strengths are consistency in learning, problem-solving, and willingness to improve. I try to understand concepts rather than simply memorize solutions."

### 5. What is your weakness?

**Sample answer:**

"Sometimes I spend more time than necessary exploring alternative approaches to a problem. I am improving by setting time limits and prioritizing a working solution before optimization."

### 6. Why should we hire you?

**Sample answer:**

"I have a good foundation in programming and computer science concepts, practical project experience, and an interest in continuous learning. I am willing to take responsibility, adapt to new technologies, and contribute to the team."

### 7. How do you handle pressure?

**Sample answer:**

"I divide the work into smaller tasks, identify priorities, and focus on solving one problem at a time. If I face a blocker, I try to understand it systematically and seek guidance when required."

### 8. What do you do when you don't know an answer?

**Sample answer:**

"I would be honest that I don't know the answer. I would try to reason through the problem using what I know and explain my thought process rather than guessing."

### 9. Are you comfortable relocating?

**Sample answer:**

"Yes, I am open to relocation based on the role and business requirements."

### 10. Where do you see yourself in five years?

**Sample answer:**

"I want to become a capable software professional with strong technical expertise, practical project experience, and the ability to take ownership of important responsibilities."

---

# 10. Complete Learning Resource Directory

## Programming Languages

| Subject | Direct Resource |
|---|---|
| Python Documentation | https://docs.python.org/3/ |
| Python Tutorial | https://docs.python.org/3/tutorial/ |
| Java Learning | https://dev.java/learn/ |
| Java Documentation | https://docs.oracle.com/en/java/ |
| C++ Reference | https://en.cppreference.com/w/ |
| SQLBolt | https://sqlbolt.com/ |

## Computer Science Fundamentals

| Subject | Direct Resource |
|---|---|
| DBMS | https://www.geeksforgeeks.org/dbms/ |
| Operating Systems | https://www.geeksforgeeks.org/operating-systems/ |
| Computer Networks | https://www.geeksforgeeks.org/computer-network-tutorials/ |
| OOP | https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/ |
| Software Engineering | https://www.geeksforgeeks.org/software-engineering/ |

## Coding Practice

| Platform | Direct Link |
|---|---|
| LeetCode | https://leetcode.com/ |
| HackerRank | https://www.hackerrank.com/ |
| GeeksforGeeks | https://www.geeksforgeeks.org/ |
| CodeChef | https://www.codechef.com/ |
| Codeforces | https://codeforces.com/ |
| NeetCode | https://neetcode.io/ |
| InterviewBit | https://www.interviewbit.com/ |

## Infosys Resources

- Infosys Careers: https://www.infosys.com/careers/
- Infosys Official Website: https://www.infosys.com/
- Infosys Springboard: https://infyspringboard.onwingspan.com/

## Interview Experience Platforms

- Glassdoor: https://www.glassdoor.co.in/Interview/index.htm
- AmbitionBox: https://www.ambitionbox.com/interviews

*Note: Candidate-reported interview experiences are not official Infosys question papers. Actual hiring stages and questions can vary.*

---

# 11. Recommended Preparation Strategy

## Phase 1 – Programming

- Select one primary programming language.
- Revise fundamentals and OOP.
- Practice coding problems.
- Understand built-in data structures.
- Practice explaining code line by line.

## Phase 2 – DSA

- Arrays and strings.
- Hashing and two pointers.
- Sliding window.
- Binary search.
- Linked lists.
- Trees and graphs.
- Recursion and backtracking.
- Greedy algorithms and dynamic programming.

## Phase 3 – Core Computer Science

- SQL queries and joins.
- DBMS and normalization.
- Transactions and ACID.
- OS processes and threads.
- CPU scheduling.
- Deadlocks and memory management.
- OSI model and TCP/UDP.
- HTTP, DNS, and IP addressing.

## Phase 4 – Projects

- Prepare a two-minute project introduction.
- Understand the complete architecture.
- Revise the database schema.
- Understand important functions and APIs.
- Explain your individual contribution.
- Prepare for project-related follow-up questions.

## Phase 5 – Mock Interviews

- Practice technical questions aloud.
- Solve coding problems within a time limit.
- Write SQL queries without looking at solutions.
- Explain your approach and complexity.
- Practice HR questions.

---

# 12. Final Interview Checklist

- [ ] Python fundamentals revised.
- [ ] Java fundamentals revised if relevant.
- [ ] OOP concepts understood.
- [ ] SQL queries practiced.
- [ ] SQL JOINs and subqueries revised.
- [ ] DBMS normalization understood.
- [ ] ACID properties revised.
- [ ] Indexing and transactions understood.
- [ ] OS process and thread concepts revised.
- [ ] CPU scheduling algorithms practiced.
- [ ] Deadlock concepts understood.
- [ ] Paging and virtual memory revised.
- [ ] OSI model memorized with explanations.
- [ ] TCP and UDP differences understood.
- [ ] DNS, HTTP, HTTPS, and IP addressing revised.
- [ ] Arrays and strings practiced.
- [ ] Linked lists and trees revised.
- [ ] Graph BFS and DFS practiced.
- [ ] Recursion and dynamic programming revised.
- [ ] Every resume project explained.
- [ ] GitHub repositories checked.
- [ ] HR questions practiced.
- [ ] At least one mock interview completed.

---

# Final Advice

Do not prepare only by memorizing answers.

For every technical concept:

1. Understand the definition.
2. Learn how it works internally.
3. Write a small example.
4. Understand its real-world use.
5. Practice explaining it in simple language.

For coding problems, always explain:

- Your approach.
- Why you selected that approach.
- Time complexity.
- Space complexity.
- Edge cases.

**The goal is not just to know the answer. The goal is to understand the concept well enough to explain it confidently and solve variations of the same problem.**

All the best for your Infosys DSE interview!
