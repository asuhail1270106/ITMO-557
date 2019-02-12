# Chapter 6

### 1. Explain the different iSCSI host connectivity options.

* Software iSCSI initiator - NIC

    * Simplest and least expensive option for iSCSI connectivity. Easily implemented since most servers come with at least one NIC. As long as your software can initiate iSCSI functionality, your NIC will do the rest.

* Software iSCSI initiator - TOE NIC

    * A TOE NIC functions similar to a regular NIC, but it alleviates certain burdens on the CPU when it offloads TCP management from the CPU.

* iSCSI HBA

    * Outperforming both above options, the iSCSI HBA offloads both TCP & iSCSI processing from the CPU. Being the easiest way to boot hosts from a SAN environment using iSCSI.

### 2. Explain the 2 types of iSCSI names.

* Native

    * Does not have FC components, initiators are directly connected to the IP network.

* Bridged

    * Implements FC components, they work in conjunction with IP. Ex. - initiators exist in IP environment while storage in FC environment.

### 3. Explain a few ways that FCIP might be used in an enterprise data center.

* It could be used to replicate data asynchronously from a local data center to a remote data center.

* It can be implemented to act as a SAN backup/archiving system.

* It can be used to simply transport data from one data center location to another physical location. This is in particular a Data Migration project.

### 4. Explain how priority-based flow control (PFC) works.

* Normal flow control or packet drop flow control is not lossless. To combat this, PFC provides a link level flow control mechanism. It creates 8 separate virtual links on a single physical link and allows freedom of operation based on user priority. Since virtual links can be paused, it allows for lossless links for traffic.

### 5. Explain how congestion notification (CN) works.

* Simply put, it is an end-to-end congestion management system. This system detects congestion and asks for traffic to be moved to a less congested line.