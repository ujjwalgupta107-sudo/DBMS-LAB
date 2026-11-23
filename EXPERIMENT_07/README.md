# Experiment 7: Functional Dependencies and Normalization (UNF to BCNF)

## Aim
To identify functional dependencies in a denormalized Sales table and normalize it step-by-step from UNF to 1NF, 2NF, 3NF, and BCNF, and to verify lossless join and dependency preservation using SQL queries.

---

## Normalization Steps Demonstrated

1. **Unnormalized Form (UNF)**:
   - Contains multi-valued attributes (`ProductList` storing multiple comma-separated items per row).
   - Violates atomicity.

2. **First Normal Form (1NF)**:
   - Deconstructs repeating groups and multi-valued fields so every cell holds an atomic (indivisible) value.
   - Identified composite candidate key: `(OrderID, ProductID)`.

3. **Second Normal Form (2NF)**:
   - In 1NF and contains no **partial functional dependencies** (no non-prime attribute depends on a proper subset of candidate key).
   - Decomposed into `Orders_2NF`, `OrderItems_2NF`, and `Products_2NF`.

4. **Third Normal Form (3NF)**:
   - In 2NF and contains no **transitive dependencies** (`X -> Y` where `Y` is non-prime and `X` is not a superkey).
   - Decomposed into distinct relations for `Customers`, `Salespersons`, `Products`, `Orders`, and `OrderItems`.

5. **Boyce-Codd Normal Form (BCNF)**:
   - For every non-trivial functional dependency `X -> Y`, `X` must be a superkey.
   - Decomposed to handle any non-trivial overlapping candidate keys if present.

6. **Lossless Decomposition Verification**:
   - Demonstrated via `NATURAL JOIN` / `INNER JOIN` ensuring reconstructed rows match original cardinality without spurious tuples.

---

## Execution
```bash
mysql -u root -p < EXPERIMENT_07/experiment_07_normalization.sql
```
