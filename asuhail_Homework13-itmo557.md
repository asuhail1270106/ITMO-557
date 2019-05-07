# Chapter 15

### 1. Explain monitoring and alerts

- Monitoring is an integral part of managing
storage infrastructure resources. It provides the performance and
accessibility status of the different components of a system and enables administrators to
perform essential management activities. Monitoring also helps to analyze the
utilization and consumption of various storage infrastructure resources. This
analysis allows for capacity planning, forecasting, and optimal use of these
resources.

- Alerts are one of the most important parts of monitoring. Alerts keeps administrators
informed about the status of various components and processes like: conditions such as failure of power, disks, memory, or switches, which
can impact the availability of services and require immediate administrative
attention.
### 2. Explain the use of charge back reports

- Charge back reports contain information about the allocation/utilization of storage infrastructure components by various departments or user groups.

- For example, the book gives the following deployment of a storage infrastructure:
    
    - Three servers with two HBAs each connect to a storage array via two switches, SW1 and SW2. Individual departmental applications run on each of the servers. Array replication technology is used to create local and remote replicas. The production device is represented as A, the local replica device as B, and the remote replica device as C.

    - There needs to be a report that documents the exact amount of storage resources used by each application via charge back analysis. If a company is billed for how much raw storage is used by an application, the report need to clarify this metric in order to keep proper record.

### 3. Explain how monitoring is used

- Monitoring provides the performance and accessibility status of the different components of a system and enables administrators to perform essential management activities.

- For example, if a network uses different pieces of networking equipment and relies on them to incorporate redundancy, the system administrator needs to know when one of the pieces of hardware becomes inaccessible. If this were to occur, there would no longer be any redundancy in the network. This is where monitoring becomes extremely important.

### 4. Explain multi-tenancy

- Through the use of virtualization, Multitenancy will allow multiple independent tenants to be serviced using the same set of storage resources. In spite of the benefits offered by multitenancy, it is still a key security concern for users and service providers. Colocation of multiple VMs in a single server and sharing the same resources increase the attack surface. It may happen that business critical data of one tenant is accessed by other competing tenants who run applications
using the same resources.