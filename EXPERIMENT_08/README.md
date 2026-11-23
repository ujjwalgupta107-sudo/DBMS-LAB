# Experiment 8: Transactions, Savepoints, Isolation Levels & Concurrency Anomalies

## Aim
To implement banking transactions using `START TRANSACTION`, `COMMIT`, `ROLLBACK`, and `SAVEPOINT`, simulate partial failures, and demonstrate isolation levels and concurrency anomalies using concurrent sessions.

---

## Concepts Demonstrated

1. **ACID Properties**:
   - **Atomicity**: Complete execution or full rollback of debit/credit operations.
   - **Consistency**: Enforcing balance invariants (`CHECK (Balance >= 0)`).
   - **Isolation**: Segregating concurrent transaction operations.
   - **Durability**: Committed data survives system resets.

2. **Transaction Control Language (TCL)**:
   - `START TRANSACTION` / `COMMIT` / `ROLLBACK`.
   - `SAVEPOINT <name>` and `ROLLBACK TO <name>` for granular partial rollbacks without aborting entire transaction scope.

3. **Transaction Isolation Levels**:
   - `READ UNCOMMITTED`: Prone to Dirty Reads.
   - `READ COMMITTED`: Eliminates Dirty Reads; prone to Non-Repeatable Reads.
   - `REPEATABLE READ` (MySQL InnoDB Default): Eliminates Non-Repeatable Reads via MVCC (Multi-Version Concurrency Control).
   - `SERIALIZABLE`: Total locking-based isolation preventing Phantom Reads.

4. **Concurrency Anomalies Simulated**:
   - Dirty Reads
   - Non-Repeatable Reads
   - Phantom Reads
   - Lost Updates

---

## Execution
```bash
mysql -u root -p < EXPERIMENT_08/experiment_08_transactions_isolation.sql
```
