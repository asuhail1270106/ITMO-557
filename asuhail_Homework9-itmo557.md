# Chapter 11

### 1. What are some of the advantages of pointer-based virtual replication?
    
    Well, pointer-based virtual replication has a few advantages, but it also has some disadvantages. Some of these revolve around the source. In pointer-based virtual replication the size of the target for replication is just a small fraction of the source compared to other replication techniques. This is possible because in pointer-based virtual replication the target contains only pointers to the data, and therefore, the physical capacity required for the target is a fraction of the source device. But, unfortunately, this means that if the source is not available, restoration is not possible. Another small advantage is that the target in pointer-based virtual replication is immediately accessible after the replication process begins.

### 2. Explain the use of pointer-based full-volume replication.
    
    Well, Pointer-Based, Full-Volume Replication provides fill copies of the source data on the targets. Immediately after the replication process, the target is made available, similar to Pointer-Based Virtual Replication.
    
    There are two modes that Pointer-Based, Full-Volume Replication can be activated in. Copy on First Access mode (CoFA) or Full Copy mode will both created a protection bitmap for all the data on the source device. This bitmap keeps track of any changes made on the source device. The target has on it, pointers that are initialized to map the corresponding data block on the source. This data is then copied from the source to the target based on which mode Pointer-Based, Full-Volume Replication was activated in.

### 3. In Continuous Data Protection, what is the importance of a journal volume? 

    The journal volume contains all the data that has changed from the time the replication session started. The amount of space that is configured for the journal determines how far back the recovery points can go.

### 4. Explain pointer-based virtual and pointer-based full-volume replication when used with CoFA mode.

    In pointer-based virtual and pointer-based full-volume replication in CoFA
    mode, access to data on the replica is dependent on the health and accessibility
    of the source volumes. If the source volume is inaccessible for any reason, these replicas cannot be used for a restore or a restart operation.

    In pointer-based full-volume replication, CoFA has some impact on performance, but with pointer-based virtual replication, there is a very high impact on performance.

### 5. Explain how a VM snapshot is used.

    VM Snapshot captures the state and data of a running virtual machine at a
    specific point in time. The VM state includes VM fi les, such as BIOS, network
    configuration, and its power state (powered-on, powered-off, or suspended).
    The VM data includes all the fi les that make up the VM, including virtual disks
    and memory. A VM Snapshot uses a separate delta fi le to record all the changes
    to the virtual disk since the snapshot session is activated.

    These VM snapshots are quite useful when your Vm needs to be reverted to the previous state it was in before some logical corruption to your files.