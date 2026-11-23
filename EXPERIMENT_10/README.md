# Experiment 10: 10,000-Row Dataset, Slow Queries and Optimization

## Aim
To generate a dataset of at least 10,000 rows, execute slow queries, analyze execution plans using `EXPLAIN`, optimize them through indexing and query rewriting, and benchmark performance before and after optimization.

---

## Concepts Demonstrated

1. **Synthetic Data Ingestion**:
   - Generating 10,000 enterprise sales rows using Recursive Common Table Expressions (`WITH RECURSIVE`).

2. **Performance Bottleneck Patterns Identified**:
   - Non-sargable predicate queries (e.g., functions wrapping indexed columns like `YEAR(SaleDate)`).
   - Leading wildcard patterns (`LIKE '%substring%'`).
   - Missing covering indexes leading to unnecessary disk / buffer pool reads.
   - Unindexed subqueries and Cartesian join penalties.

3. **Optimization Strategies Applied**:
   - Query rewriting to make predicates sargable (`SaleDate >= '2023-01-01' AND SaleDate < '2024-01-01'`).
   - Composite covering indexes allowing index-only scan without table lookups (`Using index`).
   - Rewriting `NOT IN` subqueries to `NOT EXISTS` or `LEFT JOIN ... WHERE IS NULL`.

---

## Execution
```bash
mysql -u root -p < EXPERIMENT_10/experiment_10_query_optimization.sql
```
