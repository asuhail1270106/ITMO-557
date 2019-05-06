# Chapter 14

### 1. Explain repudiation.  Give examples.

- Repudiation is an attack against the accountability of information. This attack will attempt to provide false information by pretending to be someone they're not or will try to make it seem like something which took place, didn't actually happen. In this type of attack, an adversary may attempt to perform and action, but then try to remove any evidence that could trace back to them.

- Examples:
    
    - An attacker may infiltrate a system by logging in using another user's credentials.

    - An attacker may perform unauthorized actions on a system which logs all activity, after which, the attacker may delete all log files.

### 2. Explain how Kerberos is used in a NAS environment for authentication.

- Kerberos is a network authentication protocol. It's designed to provide strong
authentication for client/server applications by using secret-key cryptography.
It uses cryptography so that a client and server can prove their identity to each
other across an insecure network connection. After the client and server have
proven their identities, they can encrypt the communication between them in order to
ensure privacy and data integrity.

- In a NAS environment, Kerberos is usually used to authenticate against a Microsoft AD domain, but can also be used to execute security functions is UNIX environments. Here are the steps:

    1. User logs in on a node in the AD domain using user/pass. The node sends request to AS running on KDC for a Kerberos ticket. KDC verifies user's login info from AD.
    2. KDC gives ticket granting ticket (TGT) and encrypted session key. TGT to be decrypted by KDC, while session key is to be decrypted by client.
    3. When client requests service from server, servers send request with prev generated TGT(encrypted with session key and containing resource info to KDC).
    4. KDC checks permissions in AD and ensures user has appropriate authorization.
    5. KDC returns service ticket to client which contains fields addressed to the client and to the server hosting the service.
    6. Client sends the service ticket to server w/ resources.
    7. The server/NAS device decrypts server portion of ticket and stores info in keytab file.
    8. Client-Server conn is active. Server returns session ID to client which monitors client activity.

### 3. Explain what can be done to increase security at the compute level.

- Physical server security involves implementing user authentication and authorization
mechanisms. These mechanisms identify users and provide access privileges
on the server. To minimize the attack surface on the server, unused hardware
components, such as NICs, USB ports, or drives, should be removed or disabled.

- The hypervisor should also be secured since it can cause all VMs installed on it to fail the case of an attack. To protect against attacks,
security-critical hypervisor updates should be installed regularly. Further, the
hypervisor management system must also be protected. Malicious attacks and
infiltration to the management system can impact all the existing VMs and
allow attackers to create new VMs. Access to the management system should be
restricted to authorized administrators. Furthermore, there must be a separate
firewall installed between the management system and the rest of the network.

- As for the Virtual Machines and guest OSs, VM isolation and hardening are commonly used security mechanisms to
effectively safeguard from an attack. VM isolation helps to prevent a compromised
guest OS from impacting other guest OSs. VM isolation is implemented
at the hypervisor level. Apart from isolation, VMs should be hardened against
security threats. Hardening is a process to change the default confi guration to
achieve greater security.

### 4. Explain what can be done to increase security at the network level.

- Firewalls are used to protect networks from unauthorized access while allowing only permitted connections. In a virtualized and cloud environment, a firewall
can also protect hypervisors and VMs. A firewall also secures VM-to-VM traffic. This
firewall service can be provided using a Virtual Firewall (VF). A VF is a firewall
service running entirely on the hypervisor. A VF provides packet filtering and
monitoring of the VM-to-VM traffic. A VF gives visibility and control over the
VM traffic and enforces policies at the VM level.

- Intrusion Detection is used to detect events that can compromise the integrity, confidentiality, or availability. A system that can be used for intrusion detection automatically analyzes events to check whether an event or a sequence of
events match a known pattern for anomalous activity, or whether it is (statistically) different from most of the other events in the system. It generates
an alert if an irregularity is detected. DMZ and data encryption are also deployed as security measures in the virtualized and cloud environments.

### 5. Explain what can be done to increase security at the storage level.

- Access control methods to regulate which users and processes access the
data on the storage systems.
- Zoning and LUN masking.
- Encryption of data-at-rest (on the storage system) and data-in-transit. Data encryption should also include encrypting backups and storing encryption keys separately from the data.
- Data shredding that removes the traces of the deleted data.
- Isolation of different types of traffic using VSANs.