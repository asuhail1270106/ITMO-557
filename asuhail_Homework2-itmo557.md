# Chapter 2

## 1. What are some benefits of computer virtualization.
When a corporation takes advantage of virtualization technology, they are able to greatly reduce the amount of money they spend on CapEx and OpEx. IT Operations that are virtualized will also minimize downtime and make disaster recovery much easier. This is because it is very easy to provision applications/tasks with virtual resources (all it takes is the click of a button). Also, if there are fewer servers utilized, there is a great deal of space that is saved in the data center. 

## 2. What are virtual machines.
A virtual machine is a computer system that is ran only using logic resources that are emulated onto physical resources. A virtual machine that is running an operating system like windows or linux will provide the exact same functionality as a physical computer.

## 3. Explain the process of concatenation as it relates to volumes.
Ok, so if we were to look at physical volumes and logical volumes, then concatenation is the process of taking __multiple physical volumes__ and concatenating them into __one logical volume__.

## 4. Explain the factors that contribute to the service time of mechanical disks.
Mechanical disks having moving parts. Therefore, there are factors that cause delays in information transfer. Mechanical disks need to deal with seek time, rotational latency, and data transfer rate.

* Seek time is the time it takes for the "arm" inside the drive to move itself over the correct track. Even though these times are measured in milliseconds, the delay adds up since information moves at the speed of light and even measurements this small are considered detrimental.
* Rotational latency refers to the delay that is caused due to information being stored on track around the platter. This means that if the arm is over one side of the platter, the platter would have to be rotated to the other side so that more information stored on the platter can be accessed.
* Data transfer rate refers to the average amount of time it takes for data from the disk to reach the host bus adapter. Since there are different components the make up a mechanical drive, there is a latency period of transfer between each component (platter→read/write heads→buffer→interface→HBA).
## 5. Explain the challenges of a DAS environment.
Even though a DAS environment is easy and simple to deploy, it is very difficult to scale. This fact alone would eliminate it as a viable option for most business needs. Reprovisioning resources in a DAS environment is a nightmare, and in most cases not possible. If the front-end ports on a storage array aren't all used, they are pretty much wasted since it's too difficult to redistribute for use with different hosts.

# Chapter 3

## 1. What is software RAID.  Give examples.
In simple terms, it is any piece of software that runs ona computer and provides limited RAID functionality (software RAID cannot mimic hardware RAID perfectly). 

Ex: mdadm is a utility in Linux that allows for the implementation of software RAID. raidtools is another tool for Linux distributions. Windows 8 has a RAID technology called Storage Spaces. 
## 2. Explain RAID-corrected IOPS on a disk for RAID 5.
Ok, so let's start with how many IOPS a specific task/application might take. If we take 5200 IOPS, as it is in the textbook, and assume a 60 percent read and 40 percent write ratio, we then look at the formula.
> (readPercentage * generatedIOPS + writepenaltyofRAID5 * (writePercentage * generatedIOPS))

This function asks us to use the read and write percentages of the task/application, the number of IOPS generated, and the write penalty of the RAID setting you're working with. For us, this would be a write penalty of 4 since we are working with RAID 5. Therefore, our final formula would look like this:
> (0.6 * 5200 + 4 * (0.4 * 5200))

> (3120 + 4 * (2080))

> (3120 + 8320)

> 11,440 IOPS

### Now, what is going on up here ↑↑↑

This formula is trying to tell us what the disk load will be on the specific RAID configuration you are using. This formula calculated a disk load of 11,440 IOPS. This means that now we can try and determine the number of disks needed to run the task/application. Assuming that each disk allows for a maximum of 180 IOPS, we would need:

> 11,440/180 = 64 disks

Therefore, the RAID corrected IOPS for this particular task/application would be 11,440 and we would need 64 disks with a max IOPS limit of 180 to handle them.

## 3. Explain write penalty in RAID 6.
Well RAID 6 has a heavy write penalty, though many storage engineers accept this as a necessary sacrifice when compared to the benefits of RAID 6. RAID 6 maintains a dual parity, this means that in terms of read operations, it needs 2 parity operations and 1 data operation. After this, there are also 3 write operations, 2 parity operations and 1 I/O operation. This means RAID 6 performs 6 I/O operation for each write. This means the write penalty for RAID 6 is 6.

## 4. What kind of applications are best suited for RAID 3.
Any applications that need large sequential data access (video/music streaming, backing up data) will receive great performance from RAID 3.
