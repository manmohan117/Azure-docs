# Virtual Machines in Azure

## What is a Virtual Machine?
A **Virtual Machine (VM)** is a compute resource that uses software instead of a physical computer to run programs and deploy applications. A VM runs as a "guest" machine on a physical "host" machine, with its own operating system, separate from other VMs. 

VMs are commonly used in cloud computing, allowing multiple users to share virtualized application resources efficiently and cost-effectively.

![VM Concept](images/vm-concept.png)

## Use Cases of Virtual Machines
- Running an OS as a separate computing environment.
- Testing applications in a sandboxed environment.
- Server virtualization for improved efficiency.
- Handling virus-infected data without affecting the host system.

## How Virtual Machines Work
A VM operates as a process within an application window on the host OS. Key components of a VM include:
- Log files
- NVRAM settings
- Virtual disk files
- Configuration files

![VM Components](images/vm-components.png)

## Advantages of Virtual Machines
✔️ Ability to run multiple OS environments on a single physical machine.  
✔️ Supports legacy applications.  
✔️ Integrated disaster recovery and provisioning.  

## Disadvantages of Virtual Machines
❌ Performance limitations when running multiple VMs on the same hardware.  
❌ Less efficient compared to physical machines.  

## Types of Virtual Machines
### 1. Process Virtual Machine
Runs a single process as an application on a host system. Example: Java Virtual Machine.

### 2. System Virtual Machine
A fully virtualized environment that mimics a physical machine. Example: VMware ESXi.

## Types of Virtualization
1. **Hardware Virtualization** - Virtual machines share a single physical server.
2. **Software Virtualization** - Enables multiple OS instances on a single host.
3. **Storage Virtualization** - Combines multiple storage resources into one.
4. **Network Virtualization** - Divides network bandwidth into independent channels.
5. **Desktop Virtualization** - Stores desktops on a remote server for remote access.

![Types of Virtualization](images/types-of-virtualization.png)

## Containers vs. Virtual Machines
| Feature        | Containers | Virtual Machines |
|---------------|------------|----------------|
| OS Isolation  | No (Shares OS Kernel) | Yes (Full OS Isolation) |
| Performance   | Lightweight & Fast | Heavier & Slower |
| Use Case      | Microservices, DevOps | Legacy Applications, OS Testing |

## Scaling Virtual Machines in Azure
Azure provides various ways to scale VMs:

### **1. Virtual Machine Scale Sets**
- Automatically deploys and manages a group of identical, load-balanced VMs.
- Ensures consistent configuration and easy scaling.

![VM Scale Sets](images/vm-scale-sets.png)

### **2. Virtual Machine Availability Sets**
- Ensures high availability by distributing VMs across multiple fault and update domains.

**Update Domains:** Ensures staggered updates to prevent simultaneous downtime.  
**Fault Domains:** Distributes VMs across different power and network resources to minimize failures.  

![Availability Sets](images/availability-sets.png)

## Examples of VM Usage in Azure
6. **Testing and Development** - Rapidly deploy different OS configurations.
7. **Running Applications in the Cloud** - Cost-effective deployment.
8. **Extending On-Premises Datacenters** - Hybrid cloud integration.
9. **Disaster Recovery** - Backup and restore critical applications in Azure.

## Moving to the Cloud with VMs
- VMs enable a "lift and shift" approach, migrating workloads from physical servers to the cloud.
- Users are responsible for maintaining the OS and software on their VMs.

## Azure VM Resources
When creating a VM, users can configure:
- **Size** (CPU, RAM)
- **Storage Disks** (HDD, SSD)
- **Networking** (Virtual Network, Public IP, Security Groups)
## How to create a Virtual Machine in Azure

- Navigate to Virtual Machines in Azure portal.

	![alt text](../../images/Pasted%20image%2020250217124224.png)

- Click Create 
	- you will have two options 
		- create a virtual machine hosted by Azure (pre configured).
		- create a virtual machine with preset configurations
	![alt text](../../images/Pasted%20image%2020250217124447.png)

- Now you will see a configuration screen with following configurations 
	- Basics 
	- Disks
	- Networking
	- Management
	- Monitoring
	- Advanced
	- Tags
	- Review + create.
		![alt text](../../images/Pasted%20image%2020250217124709.png)

#### Basics
	-project details
		-subscription
		-resource group (new or select existing)
	
- ![alt text](../../images/Pasted%20image%2020250217125222.png)
-
	-instance details
		-VM name
		- Region
		- Availibility options
		- zone options
		- security type
		- image
		- Vm architecture(Arm64 , x64)
		- Enable Hibernation.
		
- 
			![alt text](../../images/Pasted%20image%2020250217125250.png)
	-Administrator account
			authentication type 
				-SSH public key
				- password
			-username
			- SSH public key source
			- SSH key type
		-innboud Port rules
				
		
	![alt text](../../images/Pasted%20image%2020250217125321.png)

#### Disks
Azure VMs have one operating system disk and a temporary disk for short-term storage. You can attach additional data disks. The size of the VM determines the type of storage you can use and the number of data disks allowed.

- VM disk Encryption 
- OS disk
	- disk size
	- disk type
	- delete with VM
	- Enable Ultra Disk Capability
	- Data disk (add or create disk).
	- 
	
	- ![alt text](../../images/Pasted%20image%2020250217125844.png)

#### Networking
Define network connectivity for your virtual machine by configuring network interface card (NIC) settings. You can control ports, inbound and outbound connectivity with security group rules, or place behind an existing load balancing solution.

- Virtual network
- public id
- NIC network security Group
- public inbound port
- Select inbound port

	![alt text](../../images/Pasted%20image%2020250217125936.png)

- delete NIC when VM is deleted
- Enable accelerated networking
- Load Balancing
	- ![alt text](../../images/Pasted%20image%2020250217130128.png)

#### Management 


- ![alt text](../../images/Pasted%20image%2020250217130255.png)

- 




	- ![alt text](../../images/Pasted%20image%2020250217130402.png)

if you fail to choose the options correctly 

- ![alt text](../../images/Pasted%20image%2020250217130508.png)

Now if VM is created.
![alt text](../../images/Pasted%20image%2020250217170154.png)

	-Go to connect
	-choose one of the method (common -> RDP (remote desktop protocol ))
		- this will give you an Remote desktop connection.
	- now you can access the VM running Windows server 

## How to configure the VM for IIS

- Go to server Manager 
- install IIS Manager 
	- go to (add roles and features)
	- find features you want to install (IIS Manager)
	- click next... 
	after installations.....
- navigate to IIS Manager
- go to Application pool