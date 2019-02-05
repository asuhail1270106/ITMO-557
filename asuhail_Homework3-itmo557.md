# Chapter 4

## 1. Explain the different components of an intelligent storage system.
* Front End
    
    * In an intelligent storage system, the front end is the interface that allows the host to communicate with the storage system. The front end is made up of ports and controllers. The ports allow the hosts to connect to them. The controllers are in charge of these ports and allow hosts to communicate with the storage network. These controllers transport data bank and forth from cache, sending messages to the host when the data reaches cache.

* Cache

    * Cache is a type of fast, expensive memory that stores data temporarily in order to reduce the amount of time it takes to process requests from the hosts. In Intelligent Storage Systems, cache stores memory before it is send over to the hard disks. This is considered intelligent because hard disks/mechanical drives are much slower than cache.

* Back End

    * In an intelligent storage system, the back end is the interface that allows the physical disks to communicate with cache. The back end is made up of back-end ports and back-end controllers. The ports allow the physical disks to connect to them. The back-end controllers have a constant connection to the physical disks in order to aid them in read/write requests.

* Physical Disks

    * Physical disks are exactly what they sound like. They are actual physical pieces of hardware capable of storing data. These disks are connected to the back-end storage controllers which allow them to communicate with cache memory.

## 2. Explain the different kinds of flushing.

* Idle flushing

    * This type of flushing occurs continuously. Idle flushing occurs at a modest when the cache is being utilized at anywhere between a low to high watermark.

* High watermark flushing

    * As the name suggests, this type of flushing is only activated one the cache start being utilized at a high watermark. A storage system needs to assign extra resources in order to properly execute this level of flushing.

* Forced flushing

    * Uh oh, cache is being utilized at 100 percent capacity, what do you do? When input/output requests come in a large cluster and clog up the system, it allocates extra resources in order to prioritize flushing the cache.

## 3. Explain the different lun expansion techniques.

* Concatenated expansion

    * In concatenated expansion, there is additional capacity added to the base LUN. In this expansion, the base is not always the same capacity as component LUNs. Concatenated expansion is quite fast but will not improve performance.

* Striped expansion

    * Base LUN data is restriped amongst the base LUN and component LUNs. Unlike concatenated expansion, all LUNs in this expansion type must be the SAME capacity/RAID level. This expansion type allows for better performance due to the striping of an increased number of drives.

## 4. Explain LUN masking - why it is used.
LUN masking allows for data access control by defining which LUNs a host can access. It is used to prevent unauthorized/accidental volume access by hosts when in a shared environment.

## 5. Explain cache mirroring and cache vaulting.

* Cache mirroring

    * Each cache write is held in 2 different memory locations on 2 different memory cards. Cache coherency(ensuring that the data in the two different cache locations is always identical) must be maintained in cache mirroring.

* Cache vaulting

    * Simply put, in the event of a power failure, the data in cache is dumped onto physical non-volatile drives, also called vault drives. This is cache vaulting.

# Chapter 5

## 1. Explain signal attenuation.
Well, attenuation is the weakening/reduction of force. Signal attenuation occurs when data is travelling down a wire and the strength of the signal gradually gets weaker due to overriding factors.

## 2. Explain the different switched fabric ports.

* N_Port

    * This port is an end point in the fabric. Sometimes called the node port, it is a storage array port connected to a switch in a switched fabric.

* E_Port

    * Port that creates a connection between FC switches. This expansion port on an FC switch must connect with a port of the similar nature on another FC switch.

* F_Port

    * This fabric port on the switch will connect to a N_Port.

* G_Port

    * This generic port on a switch can operate as either a E_Port or F_Port. It will this out on its own when implemented.

## 3. Explain the different switched fabric login types/

* Fabric login (FLOGI)

    * This type of login is performed between an N_Port and an F_Port. It utilizes WWNN & WWPN parameters along with a FLOGI frame when talking to the login service. In return, it receives an ACC from the switch.

* Port login (PLOGI)

    * This type of login is performed between two N_Ports. A PLOGI frame is sent and the opposite N_Port sends an ACC back to the originator port.

* Process login (PRLI)

    * Similar to the PLOGI, this login type deals with FC-4 ULPs like SCSI. In this case, SCSI-related parameters are exchanged between ports.

## 4. Explain zoning -- why it is used.
Zoning is the logical segmentation of node ports within a fabric into groups that can communicate with each other as a part of their own group. It is used to decrease traffic, because if not for zoning, the fabric controller will send an RSCN to all nodes in the fabric. A big waste of resources.

## 5. Why are the benefits of using a VSAN.
They improve security, scalability, availability, and manageability. Think of a virtual computer with an OS. The benefits found in this type of implementation are similar to the benefits of a VSAN.
