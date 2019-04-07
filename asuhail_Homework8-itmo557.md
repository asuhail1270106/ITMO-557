# Chapter 10

### 1. Explain how incremental backups are used.
Incremental backups only copy new data. It's really simple, a full backup keeps backing up all your data, over and over again. An incremental backup will never be the first backup of a system. There is nothing to increment to... Therefore, after an initial full backup, incremental backups can be utilized to save system resources by only backing up the new data that has been generated. This method will take longer to restore, but cumulative backups can be utilized if this method is too stagnant.

### 2. Why would you use an image-based backup over a traditional backup in a virtualized environment?
An image-based backup operates at the hypervisor level and literally takes a snapshot of the VM as a whole. It creates a copy of the guest OS and all the data associated with it (VDI files), including the state of the VM and its applications. The backup is saved as a single file called an “image,” and this image is mounted on the separate physical machine–proxy server, which acts as a backup client. The backup software then backs up these image files normally. This absolves the backup process from the hypervisor and transfers it to the proxy server, which reduces the impact to VMs running on the hypervisor. Image-based backup enables quick restoration of a VM. Oppositely, a traditional backup will only copy data, not VM files such as the virtual BIOS file, VM swap file, logs, and configuration files. This means that in order to restore a VM, a user needs to manually re-create the VM and then restore data onto it.

### 3. Give me an example of a traditional backup environment and explain what each component does.

My computer is a traditional backup environment. I have a windows 7 VM which has a backup agent installed on it. The VM seems like a physical server to the backup agent. The backup agent will backup any data on the VM to the backup device (which just so happens to be my computer's monster 5 tera-byte hard drive).

<center><img src="images/trad bak env.png" width="200"></center>

### 4. What is source-based deduplication.
The elimination of redundant data at the source before it's backed up, BAM, nuff' said baby!