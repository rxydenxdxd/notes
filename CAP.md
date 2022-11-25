## ACID

- A transaction is a collection of instructions. To maintain the integrity of a database, all transactions must obey ACID properties.
  - **Atomicity**: A transaction is an atomic unit. Therefore, all the instructions within a transaction must successfully execute, or none of them should execute. If any of the transactions fail, the entire transaction should abort and rollback
  - **Consistency**: A database is initially in a consistent state, and it should remain in a consistent state. If any one of the sub-transaction fails and the transaction is not rolled back, the database becomes inconsistent.
  - **Isolation**: If multiple transactions are running concurrently, They should not be effected by each other. The result should be the same as the result obtained if the transactions were running sequentially.
  - **Durability**: Changes that been committed to the database should remain even in the case of software and hardware failure. For instance, if an account has a balance of Rs. 10,000, it should not be affected by hardware/software failure.

## CAP Theorem

- CAP Theorem states that a distributed database system can only guarantee two of these characteristics: **Consistency**, **Availability**, and **Partition Tolerance**.
  - **Consistency**: A system is said to be consistent when all the nodes of that database return same value. That is, if a 'Read' operation is performed simultaneously on multiple nodes connected to a consistent database, all the systems should return the most recent write operation.
  - **Availability**: Availability in a distributed database system ensures that it remains operational 100% of the time. That is, every request from the nodes must return a non-error response. ( It does not necessarily mean that the data will be consistent. )
  - **Partition Tolerance**: Partition Tolerance ensures that the system does not fail, regardless of the arbitrary number of messages are dropped or delayed between nodes in a system.
  - When a network failure happens, one has to decide between:
    - Cancel the operation and thus decrease the availability but ensure consistency.
    - Proceed with the operation and provide availability but risk consistency.

## Multi-Master Replication

- It is a method of database replication which allows data to be stored by a group of computers, and updated by any member of the group.
- The Multi-Master replication system is responsible for propagating the data modifications made by each member to the rest of the group, and resolving any conflicts that might arise between concurrent changed made by different members.

## Master Replication

- It is a method of database replication in which a single member of the group is designated as the "Master" for a given piece of data and is the only node allowed to modify that data.
- Other members wishing to modify the data must first contact the Master in order to change the data, which allows consistency among the group, but is less flexible than Multi-Master Replication.
