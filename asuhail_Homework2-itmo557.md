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


## 2. Explain RAID-corrected IOPS on a disk for RAID 5.

## 3. Explain write penalty in RAID 6.

## 4. What kind of applications are best suited for RAID 3.
