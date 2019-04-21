# Chapter 12

### 1. Explain synchronous remote replication.  When and why would you use it.

In synchronous remote replication, any "writes" that are made to the source and the remote replica/target, much be committed before the host receives a reply of "write completed". Furthermore, you can't write more data to the source until previous write operations have completed. This means that the data on the source and replica will ALWAYS be identical. Not only that, but since writes are sent to the remote site in the same order in which they are received by the source, write order in maintained...

Due to the nature of synchronous remote replication, the bandwidth required must ALWAYS be greater than any amount of write workload that may occur. Synchronous remote replication requires the source and replica to not be too far apart, in most cases, this means approximately 200 kilometers. It also depends on what kind of delay in response times the application can handle. The RPO in synchronous remote replication is almost 0 since there is always 100 percent replication. It's useful if this is what you need and you don't mind having a remote site that's close by.

### 2. Explain asynchronous remote replication.  When and why would it be used.

In asynchronous remote replication, any "writes" that are made to the source and the remote replica/target immediately results in the host receiving a reply of "write completed". In asynchronous remote replication, data is buffered at the source and transmitted to the remote site afterwards. Asynchronous replication can also implement locality of reference, which means to write to that same location, repeatedly. If the same location is written to, multiple times, in the buffer, prior to transmission to the remote site, only the final version of the data is transmitted, saving link bandwidth.

Due to the nature of asynchronous remote replication, the bandwidth required can be an average of the amount of write workload that may occur. Asynchronous remote replication allows the source and replica to be far apart, in most cases, this means they can be thousand of kilometers away. The RPO in synchronous remote replication is non-zero since there is always a buffer in replication. It's useful if this isn't a problem and you need to replicate to a remote site that's far away.

### 3. Explain cascade/multi hop three-site replication.

In cascade/multihop three-site replication, data flows from the source to the
intermediate storage array, called a bunker, in the first hop. From here, data at the bunker moves to a storage array at a remote site in the second hop. Replication between the source and the remote sites can be performed in two ways: synchronous +
asynchronous or synchronous + disk buffered. Replication between the source
and bunker occurs synchronously, but replication between the bunker and the
remote site can be done using disk-buffered mode or asynchronous mode.

### 4. Explain hypervisor-to-hypervisor VM migration.

In hypervisor - to - hypervisor VM migration, the entire VM is moved from one hypervisor to another, with it's active state fully preserved. This method involves copying the contents of virtual machine memory from the source hypervisor to the target and then transferring the control of the VM’s disk files to the target hypervisor. Because the virtual disks of the VMs are not migrated, this technique requires both source and target hypervisor access to the same storage. vMotion is an excellent software to do this. The VMs in this case, need to be clustered and given access to the same storage...