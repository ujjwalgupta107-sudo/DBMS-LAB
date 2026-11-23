# Experiment 9: Indexing and Query Performance Comparison using EXPLAIN

## Aim
To create a Railway Booking table with at least 5,000 records, benchmark query performance before and after creating single-column and composite indexes, and compare execution plans using `EXPLAIN`.

---

## Concepts Demonstrated

1. **Large Dataset Generation**:
   - Generated 5,000+ realistic reservation records using MySQL 8.0 Recursive CTE (`WITH RECURSIVE`).

2. **Index Architectures**:
   - Primary Key clustered B-Tree index.
   - Single-column secondary indexes (e.g., `JourneyDate`, `PassengerName`).
   - Composite / multi-column index (e.g., `(SourceStation, DestinationStation, JourneyDate)`).

3. **Query Execution Plan Analysis (`EXPLAIN`)**:
   - Access types compared: `ALL` (full table scan) vs `range` (index range scan) vs `ref` (non-unique index lookup).
   - Cost metrics: evaluated `rows` examined and filtering efficiency.
   - Leftmost Prefix matching rule for composite indexes.

---

## Execution
```bash
mysql -u root -p < EXPERIMENT_09/experiment_09_indexing_explain.sql
```
