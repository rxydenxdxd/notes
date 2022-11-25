## Distributed Database System

- A Distributed database is a type of database in which data is stored across different physical locations.
- A distributed database is a collection of multiple interconnected databases, which are spread physically across various locations that communicate via computer network.
- It may be stored in multiple computers located in the same physical location or maybe dispersed over a network of interconnect computers.

### Types of Distributed Databases

- **Homogeneous Database**: In a homogeneous database, all different sites store database identically. The OS, DBMS and the data structures used - all are same at all sites.
- **Heterogeneous Database**: In a heterogeneous distributed database, different sites can use different schema and software than can lead to problems in query processing and transactions.

## Need for switching over to DDBMS

- **Distributed Nature of Organizational Units**
  - Most of the organization in today's world are physically subdivided into multiple units which is spread around the world.
  - Therefore each unit requires its own set of local data.
- **Support for both OLAP and OLTP**
  - OLAP (Online Analytical Processing) and OLTP (Online Transaction Processing) works over diversified systems which may have common data. DDBMS aids both of these by providing synchronous data.
- **Database Recovery**
  - Most commonly used technique of DDBMS is 'Replication'. The data stored in the DDBMS can be replicated and stored at various sites. Therefore, Even if one site is gets damaged, All the users/nodes can access the data from other sites while the failed site is being reconstructed. Thus, Database Failure is rare.

## Advantages of Distributed Database System

- **Increased Availability**: In DDBMS, the data is stored over multiple sites. Therefore, if one site gets damaged, the users/nodes can still access the information from a different site, which results in increased availability.
- **Easier Expansion**: In DDBMS, expansion of systems in terms of adding more data, increasing database sizes, adding more processing power is easier.
- **Modular Development**: Expansion of a Centralized Database System can rise conflict and may result in unavailability of the system for a certain period of time. However, in Distributed Database System, Expansion process only requires adding more computers, storing the local data into the new site, and finally connecting that site to the DDBMS.
- **More Reliable**: In case of system failures in a Centralized Database System, The database comes to a halt. However, In DDBMS, when a system/component fails, the system continues due to the propagation of data over various sites. Therefore DDBMS is more reliable.

## Disadvantages of Distributed Database System

- It is comparatively costlier to manage DDBMS as the data needs to be spread across various sites.
- When compared to CDMS, It is easier to achieve consistency over all the nodes in the network.

## Ways of Spreading Data over DDBMS

- **Replication**
  - In this approach, the same data is copied over two or more sites.
  - This approach ensures availability of data at all times.
  - However, In this approach, If there is change in one site, Then there is a need for copying that change over all the remaining sites which results in overhead.
  - Also concurrency becomes way more complex as concurrency needs to be checked over multiple sites.
- **Fragmentation**
  - In this approach, the data is fragmented (divided into smaller parts) and each of the fragments is stored in different sites where they're required. It is made sure that the data is fragmented in such as a manner that it is easier to reconstruct the original data.
  - It is advantageous as it doesn't create copies of data, and hence, consistency is not a problem.
- In certain cases, the hybrid of Replication and Fragmentation is used.

## Centralized Database System

- A Centralized Database is a type of database in which the entire data is stored at only one location.
- The Centralized Databases is accessed via an internet connection (LAN, WAN, etc.)
- This type of database system is generally used in institutions and organizations.

## Advantages of Centralized Database System

- It is cheaper than DDBMS as the location is stored at one location only.
- It is easier to access and co-ordinate.
- Data redundancy is minimum as the entire data is stored at one location only.

## Disadvantages of Centralized Database System

- The data traffic in this type of database system is high, because the data is stored at only one location.
- If there is any failure in Centralized Database System, then the entire data will be destroyed.
- In case of system failure, the users don't have any access to the data until the failure is addressed.

## Difference between DDBMS and CDBMS

| CDBMS                                                                                                                              | DDBMS                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| In this type of database, the data is stored over various sites/locations.                                                         | In this type of database, the data is stored at one location only.                                     |
| It is easier to establish a CDBMS                                                                                                  | It is comparatively costlier to establish a DDBMS                                                      |
| The management, modification, and backup procedure is easier in this type of database as the entire data is stored at one location | It is harder to perform these processes in DDBMS, As the data is spread over numerous sites/locations. |

## Strategies and Objectives of DDBMS

- Data Fragmentation
- Data Allocation
- Data Replication
- Location Transparency
