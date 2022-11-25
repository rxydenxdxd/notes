## ACID

- A transaction is a collection of instructions. To maintain the integrity of a database, all transactions must obey ACID properties.
  - **Atomicity**: A transaction is an atomic unit. Therefore, all the instructions within a transaction must successfully execute, or none of them should execute. If any of the transactions fail, the entire transaction should abort and rollback
  - **Consistency**: A database is initially in a consistent state, and it should remain in a consistent state. If any one of the sub-transaction fails and the transaction is not rolled back, the database becomes inconsistent.
  - **Isolation**: If multiple transactions are running concurrently, They should not be effected by each other. The result should be the same as the result obtained if the transactions were running sequentially. **Durability**: Changes that been committed to the database should remain even in the case of software and hardware failure. For instance, if an account has a balance of Rs. 10,000, it should not be affected by hardware/software failure.

## CAP Theorem

- CAP Theorem states that a distributed database system can only guarantee two of these characteristics: **Consistency**, **Availability**, and **Partition Tolerance**.
  - **Consistency**: A system is said to be consistent when all the nodes of that database return same value. That is, if a 'Read' operation is performed simultaneously on multiple nodes connected to a consistent database, all the systems should return the most recent write operation.
  - **Availability**: Availability in a distributed database system ensures that it remains operational 100% of the time. That is, every request from the nodes must return a non-error response. ( It does not necessarily mean that the data will be consistent. )
  - **Partition Tolerance**: Partition Tolerance ensures that the system must continue to operate regardless of the arbitrary number of messages being dropped (or delayed) by the network between the nodes.
  - When a network partition failure happens, one has to decide between:
    - Cancel the operation and thus decrease the availability but ensure consistency
    - Proceed with the operation and thus provide availability but risk consistency
  - One has to choose between availability and consistency in distributed database system.