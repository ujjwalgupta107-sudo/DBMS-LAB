# 🗄️ Database Management Systems (DBMS) Laboratory Manual

[![MySQL](https://img.shields.io/badge/MySQL-8.0%2B-00758F?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![SQL Standard](https://img.shields.io/badge/SQL-ANSI%20SQL--92%20%2F%2099-orange?style=for-the-badge)](https://en.wikipedia.org/wiki/SQL)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-blue?style=for-the-badge)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-Academic%20Use-green?style=for-the-badge)](#)

A comprehensive, production-grade repository of university Database Management System (DBMS) practical laboratory experiments implemented in **MySQL 8.0+**. 

Contains fully tested, idempotent SQL scripts, relational schemas, ER diagrams, synthetic performance datasets, execution plans, and academic documentation spanning fundamental relational constraints to advanced recursive CTEs, transactional isolation levels, B-tree index benchmarking, and query optimization.

---

## 👤 Author Information

- **Student Name**: Ujjwal Gupta
- **Roll Number**: 25LBCS3125
- **Course**: Database Management Systems (DBMS) Practical Laboratory
- **Platform**: MySQL Server 8.0+ / InnoDB Engine
- **GitHub Repository**: [ujjwalgupta107-sudo/DBMS-LAB](https://github.com/ujjwalgupta107-sudo/DBMS-LAB.git)

---

## 📚 Complete Table of Experiments

| # | Experiment Title | Target Database | Core Concepts & Techniques | Artifacts & Scripts |
|:---:|---|:---:|---|:---:|
| **01** | **ER Diagram & Relational Schema Design** | N/A | Entity Sets, Weak/Strong Entities, Attributes, Cardinality, PK/FK Mapping | [Diagram](EXPERIMENT_01/Experiment%201%20draw.io.png) • [Doc](EXPERIMENT_01/README.md) |
| **02** | **College DB & Referential Integrity Constraints** | `CollegeDB` | Primary Key, Foreign Key, `ON DELETE SET NULL`, `ON DELETE CASCADE`, `UNIQUE`, `NOT NULL` | [Script](EXPERIMENT_02/experiment_02.sql) • [Doc](EXPERIMENT_02/README.md) |
| **03** | **Employee Queries & Group Aggregations** | `CompanyDB_Exp03` | Selection (`WHERE`), Projection, `COUNT`, `AVG`, `GROUP BY`, `HAVING`, `CASE`, `ORDER BY` | [Script](EXPERIMENT_03/experiment_03.sql) • [Doc](EXPERIMENT_03/README.md) |
| **04** | **Joins, Subqueries & EXPLAIN Execution Plans** | `CompanyDB_Exp04` | `INNER JOIN`, `LEFT JOIN`, Self-Join, 3-Way Join, Correlated Subqueries, `EXISTS`, Simulated `INTERSECT`/`EXCEPT`, `EXPLAIN` | [Script](EXPERIMENT_04/experiment_04.sql) • [Doc](EXPERIMENT_04/README.md) |
| **05** | **Views, Updatability & Recursive CTEs** | `CompanyDB_Exp05` | Updatable vs Non-Updatable Views (MySQL Error 1288), View Constraints, `WITH RECURSIVE` CTE Managerial Hierarchy | [Script](EXPERIMENT_05/experiment_05.sql) • [Doc](EXPERIMENT_05/README.md) |
| **06** | **Stored Procedures, Validation & Audit Triggers** | `CompanyDB_Exp06` | Stored Procedures, `DELIMITER`, `SIGNAL SQLSTATE`, `BEFORE UPDATE` Validation Trigger, `AFTER UPDATE` Audit Logging | [Script](EXPERIMENT_06/experiment_06.sql) • [Doc](EXPERIMENT_06/README.md) |
| **07** | **Functional Dependencies & Normalization** | `DBMS_Exp7` | UNF, 1NF, 2NF (Partial Dependencies), 3NF (Transitive Dependencies), BCNF Decomposition, Lossless Join Verification | [Script](EXPERIMENT_07/experiment_07_normalization.sql) • [Doc](EXPERIMENT_07/README.md) |
| **08** | **Transactions, Savepoints & Concurrency Control** | `DBMS_Exp8` | ACID Guarantees, `START TRANSACTION`, `COMMIT`, `ROLLBACK`, `SAVEPOINT`, Isolation Levels, Concurrency Anomalies | [Script](EXPERIMENT_08/experiment_08_transactions_isolation.sql) • [Doc](EXPERIMENT_08/README.md) |
| **09** | **Indexing & Query Performance with EXPLAIN** | `DBMS_Exp9` | 5,000-Row Dataset Generation, Clustered vs Secondary Indexes, Composite Index Leftmost Prefix Rule, `EXPLAIN` Cost Comparison | [Script](EXPERIMENT_09/experiment_09_indexing_explain.sql) • [Doc](EXPERIMENT_09/README.md) |
| **10** | **Query Optimization & Performance Tuning** | `DBMS_Exp10` | 10,000-Row Ingestion, Sargable Predicates, Wildcard Optimization, Covering Indexes (`Using index`), Subquery Rewriting | [Script](EXPERIMENT_10/experiment_10_query_optimization.sql) • [Doc](EXPERIMENT_10/README.md) |

---

## 📁 Repository Structure

```
DBMS-LAB/
├── .gitignore                                      # Git ignore specifications
├── README.md                                       # Master laboratory manual (this file)
│
├── EXPERIMENT_01/                                  # Exp 1: ER Modeling & Schema Design
│   ├── Experiment 1 draw.io.png                    # High-resolution conceptual ER diagram
│   └── README.md                                   # ER mapping theory & key concepts
│
├── EXPERIMENT_02/                                  # Exp 2: College Database & Constraints
│   ├── experiment_02.sql                           # Idempotent MySQL implementation
│   └── README.md                                   # Schema documentation & referential actions
│
├── EXPERIMENT_03/                                  # Exp 3: Selection, Grouping & Aggregates
│   ├── experiment_03.sql                           # 30-record dataset & complex queries
│   └── README.md                                   # Query explanation & grouping logic
│
├── EXPERIMENT_04/                                  # Exp 4: Joins, Nested Subqueries & EXPLAIN
│   ├── experiment_04.sql                           # Multi-table joins & subquery patterns
│   └── README.md                                   # Execution plan analysis & set operations
│
├── EXPERIMENT_05/                                  # Exp 5: SQL Views & Recursive CTEs
│   ├── experiment_05.sql                           # View updatability tests & recursive reporting
│   └── README.md                                   # Updatability rules & tree traversal docs
│
├── EXPERIMENT_06/                                  # Exp 6: Stored Procedures & Triggers
│   ├── experiment_06.sql                           # Procedures, signal handling & audit triggers
│   └── README.md                                   # Procedural logic & trigger audit schema
│
├── EXPERIMENT_07/                                  # Exp 7: Relational Normalization
│   ├── experiment_07_normalization.sql             # UNF to BCNF step-by-step SQL decomposition
│   └── README.md                                   # Functional dependencies & lossless joins
│
├── EXPERIMENT_08/                                  # Exp 8: Transactions & Concurrency
│   ├── experiment_08_transactions_isolation.sql    # TCL, savepoints & isolation anomaly tests
│   └── README.md                                   # ACID properties & isolation matrix
│
├── EXPERIMENT_09/                                  # Exp 9: Indexing & Benchmarking
│   ├── experiment_09_indexing_explain.sql          # 5k row generation & index benchmarking
│   └── README.md                                   # B-Tree indexing & scan cost breakdown
│
├── EXPERIMENT_10/                                  # Exp 10: Query Optimization
│   ├── experiment_10_query_optimization.sql        # 10k dataset & 5 query rewrites with EXPLAIN
│   └── README.md                                   # Bottleneck mitigation & covering indexes
│
└── Ujjwal docs/                                    # Student lab report submissions (.docx)
    ├── DBMS ujjwal ex 7.docx                       # Submission report for Exp 7
    ├── DBMS ujjwal ex 8.docx                       # Submission report for Exp 8
    ├── DBMS ujjwal ex 9.docx                       # Submission report for Exp 9
    ├── DBMS ujjwal ex 10.docx                      # Submission report for Exp 10
    ├── RDBMS EX 3 Ujjwal Gupta 25LBCS3125.docx     # Submission report for Exp 3
    ├── RDBMS EX 4 Ujjwal Gupta 25LBCS3125.docx     # Submission report for Exp 4
    ├── RDBMS EX 5 Ujjwal Gupta 25LBCS3125.docx     # Submission report for Exp 5
    └── RDBMS EX 6 Ujjwal Gupta 25LBCS3125.docx     # Submission report for Exp 6
```

---

## ⚙️ Prerequisites & Environment Setup

- **Database Engine**: MySQL Community Server 8.0 or newer (Compatible with 8.0.x and 8.4 LTS).
- **Default Storage Engine**: `InnoDB` (Required for transaction support, foreign key referential integrity, and row-level locking).
- **Client Tools**:
  - MySQL Command-Line Client (`mysql`)
  - MySQL Workbench 8.0+
  - DBeaver / DataGrip / VS Code MySQL extension
- **Standards & Conventions**:
  - ANSI SQL-92 / ANSI SQL-99 compliance.
  - Client delimiters (`DELIMITER $$`) for stored routines and triggers.
  - Safe recursion depth settings (`SET SESSION cte_max_recursion_depth`) for synthetic dataset generation.

---

## 🚀 Execution Guide

All SQL scripts are **fully self-contained, idempotent, and re-runnable**. Each experiment automatically provisions its designated schema and drops existing objects before recreating them.

### Method 1: Using Terminal / PowerShell

Clone the repository and run any experiment via the MySQL CLI:

```bash
# Clone the repository
git clone https://github.com/ujjwalgupta107-sudo/DBMS-LAB.git
cd DBMS-LAB

# Execute individual experiments
mysql -u root -p < EXPERIMENT_02/experiment_02.sql
mysql -u root -p < EXPERIMENT_03/experiment_03.sql
mysql -u root -p < EXPERIMENT_04/experiment_04.sql
mysql -u root -p < EXPERIMENT_05/experiment_05.sql
mysql -u root -p < EXPERIMENT_06/experiment_06.sql
mysql -u root -p < EXPERIMENT_07/experiment_07_normalization.sql
mysql -u root -p < EXPERIMENT_08/experiment_08_transactions_isolation.sql
mysql -u root -p < EXPERIMENT_09/experiment_09_indexing_explain.sql
mysql -u root -p < EXPERIMENT_10/experiment_10_query_optimization.sql
```

### Method 2: Using MySQL Workbench

1. Launch **MySQL Workbench** and establish connection to your MySQL Server instance.
2. Open any script: **File** > **Open SQL Script...** (or `Ctrl+O`).
3. Execute the script: Press **Execute** (⚡) or `Ctrl+Shift+Enter`.
4. Review the generated tables, query projection grids, and `EXPLAIN` execution plans in the result panel.

---

## 🧠 Comprehensive Technical Highlights

### 1. Referential Integrity Enforcement (`ON DELETE SET NULL` vs `CASCADE`)
- **Experiment 2** highlights the distinct semantics of foreign key referential cascades.
- `Student(Dept_Id) -> Department(Dept_Id)` employs `ON DELETE SET NULL` to retain student records when departments dissolve.
- `Enrollment(Student_Id, Course_Id)` uses `ON DELETE CASCADE` to clean up invalid relational joins when an entity is permanently purged.

### 2. Logical Query Processing: `WHERE` vs `HAVING`
- **Experiment 3** contrasts predicate row filtering evaluated before aggregation (`WHERE`) against post-aggregation group filtering (`HAVING`).
- Demonstrates conditional classification with searched `CASE` statements to categorize employee remuneration bands.

### 3. Join Strategies & Query Plan Profiling (`EXPLAIN`)
- **Experiment 4** explores relational algebra operations across multiple tables.
- Explains the cost implications of `DEPENDENT SUBQUERY` in correlated nested queries versus relational `JOIN` operations.
- Implements simulated relational set operations (`INTERSECT` and `EXCEPT`) compatible with all MySQL version permutations using `IN` and `NOT IN` subqueries.

### 4. View Updatability Invariants & Recursive Hierarchical CTEs
- **Experiment 5** demonstrates MySQL Error 1288 conditions: views containing aggregate expressions (`SUM`, `AVG`), `GROUP BY`, or `DISTINCT` are inherently non-updatable.
- Leverages ANSI SQL `WITH RECURSIVE` CTE syntax to traverse hierarchical organizational trees starting from root directors (`Manager_ID IS NULL`) down to frontline personnel.

### 5. Transactional Integrity, Custom Exception Signals & Audit Logging
- **Experiment 6** establishes business logic enforcement in the database layer.
- Uses `SIGNAL SQLSTATE '45000'` to fail invalid departmental reassignments with clean, descriptive error messages.
- Pairs `BEFORE UPDATE` data validation (preventing negative compensation values) with `AFTER UPDATE` historical audit trails tracking modifications with actor and timestamp records.

### 6. Relational Normalization & Lossless Join Verification
- **Experiment 7** provides a structured decomposition of denormalized sales data across relational normal forms:
  - **UNF**: Eliminates repeating multi-valued string arrays into atomic tuples.
  - **1NF**: Establishes atomic domains with composite candidate key `(OrderID, ProductID)`.
  - **2NF**: Removes partial key functional dependencies.
  - **3NF**: Purges transitive non-prime dependencies into dedicated reference tables (`Customers`, `Salespersons`, `Products`).
  - **BCNF**: Guarantees that every determinant is a superkey.
  - Verifies lossless reconstruction using `NATURAL JOIN` / `INNER JOIN` without generating spurious rows.

### 7. ACID Transaction Control & Isolation Level Anomalies
- **Experiment 8** simulates transactional workflows using banking account debit and credit operations.
- Employs `SAVEPOINT` and `ROLLBACK TO SAVEPOINT` to perform resilient, partial error recovery.
- Analyzes concurrency phenomena across isolation tiers:
  - **Dirty Reads** under `READ UNCOMMITTED`.
  - **Non-Repeatable Reads** under `READ COMMITTED`.
  - **Repeatable Reads** guaranteed by InnoDB MVCC snapshot reads under `REPEATABLE READ`.
  - **Phantom Read Prevention** via next-key locking under `SERIALIZABLE`.

### 8. B-Tree Index Architecture & Performance Benchmarking
- **Experiment 9** benchmarks query execution across a 5,000-record dataset generated in real time using recursive CTEs.
- Evaluates cost metrics reported by `EXPLAIN`:
  - Full table scans (`type: ALL`).
  - Index range scans (`type: range`).
  - Secondary index key lookups (`type: ref`).
  - Demonstrates the **Leftmost Prefix Rule** for composite indexes `(SourceStation, DestinationStation, JourneyDate)`.

### 9. Query Bottleneck Profiling & Optimization Techniques
- **Experiment 10** identifies and resolves five classic enterprise performance anti-patterns on a 10,000-row sales dataset:
  - Eliminating non-sargable functions (`YEAR(SaleDate)`) by rewriting predicates into indexed date range comparisons.
  - Replacing leading wildcard scans (`LIKE '%xyz%'`) with prefix filters or dedicated fulltext search patterns.
  - Designing composite **Covering Indexes** that satisfy entire query projections directly within the B-Tree leaf nodes (`Using index`), avoiding clustered index disk lookups.
  - Transforming unindexed `NOT IN` subqueries into high-performance `NOT EXISTS` or anti-joins.

---

## 📌 Integrity & Academic Adherence

All practical implementations have been developed and structured according to standard university DBMS curriculum guidelines. SQL scripts adhere to ANSI standards and MySQL best practices, prioritizing idempotency, data consistency, and optimal execution performance.
