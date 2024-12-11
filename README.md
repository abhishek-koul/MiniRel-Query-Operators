Mini-Rel Stage 6: Query Optimization and Execution
This project is part of the Mini-Rel database system and focuses on implementing query optimization and execution strategies. The goal is to process SQL queries efficiently by generating and executing optimized query plans. The project involves various components such as query parsing, plan generation, and execution of relational operators.

Project Overview
The key components of this project include:

Query Parsing: Convert SQL statements into an intermediate representation.
Query Optimization: Generate and optimize query execution plans to reduce the cost of query execution.
Execution Plan: Implement relational operators to carry out query execution.
Relational Operators: Implement key operators such as selection, projection, and join.

Features
Query Parsing
Parses SQL queries and converts them into an abstract syntax tree (AST).
Validates queries to ensure correct syntax and attribute references.

Query Optimization
Generates multiple query plans and selects the most efficient one based on estimated costs.

Optimizations include:
Join Ordering: Reorders joins to minimize intermediate result sizes.
Push-Down Predicates: Applies selection and projection early in the query plan to reduce data size.

Execution Plan
Represents the sequence of relational operators needed to execute the query.
Supports both logical plans (describing operations conceptually) and physical plans (describing how operations are implemented).

Relational Operators
Selection
Filters tuples based on specified conditions.
Projection
Reduces the number of attributes in the result by selecting only relevant columns.
Join
Combines tuples from two relations based on a specified condition.
Supports various join algorithms such as nested loop join and hash join.

Query Execution
Executes the optimized plan by iterating over relational operators.
Handles large datasets efficiently by utilizing in-memory buffers and minimizing I/O operations.

Important Functions
parser.C
Converts SQL statements into an internal query representation.
Handles syntax errors and attribute validation.
optimizer.C
Generates and optimizes query plans.
Implements cost-based optimization techniques for join ordering and predicate push-down.
executor.C
Executes the query plan using relational operators.
Manages data flow between operators and handles I/O operations.
operators.C
Implements core relational operators (selection, projection, join).
Optimizes operator performance through efficient data access and memory management.
buffer_manager.C
Manages in-memory buffers to minimize disk access during query execution.
Implements page caching and buffer pinning to optimize performance.
Testing
The test_query.C file includes test cases to verify query parsing, optimization, and execution.
Sample queries are provided to test the system’s ability to process various types of SQL queries efficiently.
Project Experience
This project provided practical experience with query optimization, execution plans, and relational operator implementation. It reinforced concepts such as cost-based optimization, efficient data access, and query execution strategies in relational databases.