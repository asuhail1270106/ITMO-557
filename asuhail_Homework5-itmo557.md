# Chapter 7

### 1. Explain the benefits of a NAS.

* Comprehensive access to information: 

    * NAS is very efficient at file sharing. Supporting many-to-one and one-to-many configurations, it allows NAS devices to serve many clients simultaneously and allows one client to connect with many NAS devices simultaneously via many-to-one and one-to-many configurations respectively.

* Improved efficiency: 

    * NAS can outperform a general-purpose file server since it uses an OS optimized for file serving.

* Improved flexibility: 
    
    * Compatible with clients on both UNIX and Windows platforms using industry-standard protocols. NAS can serve requests from different types of clients from the same source.

* Centralized storage: 

    * NAS centralizes data storage to minimize data duplication on client workstations ensuring greater data protection.
    
* Simplified management: 

    * Provides a centralized console that makes it possible to manage fi le systems efficiently.
    
* Scalability: 

    * Scales well with different utilization profiles and types of business applications because of the high-performance and low-latency design.

* High availability: 

    * Allows for high availability by replicating and recovering efficiently. NAS uses redundant components that provide maximum connectivity options. A NAS device supports clustering technology for fail over.

* Security: 

    * Ensures security, user authentication, and file locking with industry-standard security schemas.

* Low cost: 

    * NAS uses commonly available and inexpensive Ethernet components.

* Ease of deployment: 

    * Configuration at the client is minimal, because the clients have required NAS connection software built in.

### 2. Explain all the components of a NAS.

* A NAS device is comprised of two main components: a NAS head and storage.

    * The NAS head is made up of: CPU & Memory, multiple NICs (provide connectivity to the client network), an OS optimized to manage NAS functionality (translates file-level requests to block-storage requests and vice versa), file sharing protocols (NFS, CIFS, etc.), and Industry-standard storage protocols & ports to connect & manage physical dick resources.

    * Storage is made up of either internal hardware or external devices shared w/ other hosts.

### 3. Explain the different NAS implementations.

* Unified: Consolidates NAS & SAN based data access within a single, unified storage platform. Management interface is unified to handle both environments.

* Gateway: NAS device uses external storage to store & retrieve data. Has separate admin tasks for NAS device and storage.

* Scale-out: NAS implementation pools multiple nodes together in a cluster. Node = NAS head, Storage, or both. Cluster performs as single entity.

### 4. Explain the benefits of file-level virtualization.

* File-level virtualization eliminates the dependencies between the data accessed at the file level and the location where the files are physically stored. Used heavily in NAS & File-Server environments, it provides non-disruptive file mobility to optimize storage utilization, simplifying it in the process.