

## INTRODUCTION TO NETWORKING

Computer Network is required to send the data from one place to another.Two remote machine can communication with each other through a process called networking. The communication means exchange of data with the help of set of protocols and networking devices.

Computer network mainly consist of two parts. One is the software and other is the hardware. The software is a stack of computer network protocols. The hardware part is collection of devices such as cable, switch, hub, router etc.In simple terms, protocols are a set of rules. Those rules are to be followed by each entity of computer network.

Any Computer Networking communication need a sender, a receiver and a communication medium to transfer signal or Data from sender to the receiver. One needs sender, receiver, communication channel, protocols and operating system to establish a computer networking.

## What is Data Communication?

when two computers exchange the information using some set of rules and networking devices, the process is said to be data communication. The information is presented in the form of data. The data may take various forms such as text, audio, video, images etc.

### To have successful data communication, it must satisfy several characteristics.

#### (1) Correctness of data communication

The data which sender has transmitted, receiver must receive the same data bit by bit. There must not be a single bit in error.

#### (2) Timeliness

Data must be received timely. The data are not useful if it arrives out of time. It means that sender and receiver must be synchronized with the order of transmission and receiving. The sender might have sent the whole message in the several units. The receiver must receive the whole message in the same sequence of units.
For example, sender is sending the video message to the receiver. The whole video message is transmitted in small parts. Then receiver can understand the message if all parts of the video message arrives at receiver in the sequence. This is applicable for audio form of the message too.

#### (3) Correct destination

The data must be received by the machine to which data actually has been transmitted. It must not reach to any other destination.

## COMPONENTS OF NETWORKING

**Computer network consists of components such as data, software, hardware, Operating system etc.**

- **Hub**: Hub is a central device to which all machines are connected. Whenever a sender machine transmits the message, it is sent through the hub. The hub is kind of broadcasting device. So it will receive the request and transmit it to the entire network. The intended receiver will accept the message and all other computers will ignore the message. It is used for N-to-N communication. Here, N indicates all computers of the network.

- **Switch**: Switch is networking device as one of computer network components. It looks like hub but it does not work similar to the hub.It has got built-in memory and intelligence. It sends the data to the specific receiver. It uses physical device addresses in each incoming messages so that it can deliver the message to the right destination or port. It is used for point-to-point (P-to-P) communication. Here, P indicates identificationof a specific computer.Both switch and hub have common features: Multiple RJ-45 ports, power supply and connection lights.

- **Router**: Routers are mainly used to send the message from source machine to the destination machine. There is a large number of routers are connected among themselves. Hence, there may be several alternative paths from source router to the destination router. Router finds the best possible path between them using routing algorithms and routing table information. Router tables are used to stores information of other neighbour routers in the network. Router also can be used to connect LANs, MANs or WANs.

	-  **Routing Algorithms**: Routing algorithms are important in the computation of the best routes through which data packets in a network should pass through. Depending on the nature of their implementation they are classified as Adaptive (Dynamic) and Non-Adaptive (Static).
	![[Pasted image 20250213171208.png]]
	- 
 - **Category 1:Algorithms that self-organize with reference to current network conditions
 
 - **Category 2: Algorithms that follow planned pathways regardless of current network conditions. It therefore becomes important to understand these differences in order to be able to fine-tune the network for maximum efficacy, and stability.
 
	 -  **Adaptive Routing algorithm**: The routing decisions are made based on network traffic and topology. The parameters that are used in adaptive routing algorithms are distance, hop, estimated transit time and count.

	-   **Non-Adaptive Routing algorithm**: The routing decisions are not made based on network traffic and topology. This algorithm is used by static routing. Non-adaptive routing algorithms are simple as compared to Adaptive routing algorithms in terms of complexity.
	|Adaptive Routing algorithm|Non-Adaptive Routing algorithm|
	|---|---|
	|An adaptive algorithm involves routers for exchanging and updating router table data.|A non-adaptive algorithm involves a network administrator for the manual entry of the routing paths into the router.|
	|This algorithm creates a routing table based on network conditions.|Whereas this algorithm creates a static table in order to determine when to send packets and which node.|
	|This algorithm is used by dynamic routing.|Whereas this algorithm is used by static routing.|
	|In adaptive routing algorithm, the routing decisions are made based on network traffic and topology.|Whereas in a non-adaptive routing algorithm, the routing decisions are not made based on network traffic and topology.|
	|Adaptive routing algorithms are more complex as compared to non-adaptive routing algorithms in terms of complexity.|While non-adaptive routing algorithms are simple in terms of complexity.|
	|In adaptive routing algorithm, the routing decisions are not static tables.|While in non-adaptive routing algorithm, the routing decisions are static tables.|
	|Adaptive routing algorithm is categorized into distributed, centralized and isolation algorithm.|Whereas non-adaptive routing algorithm is categorized into random walks and flooding.|
	|Adaptive routing algorithm is more used as compared to non-adaptive.|Whereas non-adaptive routing algorithm is comparatively less used.|
	|The dynamic protocols are employed to update the routing table and determine the best route between the source and destination computers.|The manual setup is performed for establishing an optimal path between the source and destination computers.|
	|It is mostly used for-<br><br>- Open, Complex network topologies|It is mostly used for-<br><br>- Simple, Closed network topologies|
	|Purposes-<br><br>- Enhancement in network performance<br>- Prevents packet delivery failure<br>- Aid in controlling congestion|Purposes-<br><br>- It enables fine-grained control over packet paths.<br>- Suited for reliable networks with stable loads|
	
	
	
	
	#### ****Advantages of Adaptive Routing Algorithms****
	
	- ****Dynamic:**** Adaptive routing algorithms can adjust to changing network conditions, such as traffic congestion, link failures, and topology changes, by selecting a better path for the data packets. This results in better network performance, higher throughput, and reduced latency.
	- ****Load Balancing:**** Adaptive routing algorithms can distribute network traffic across multiple paths to avoid congestion and ensure that all network links are utilized efficiently.
	- ****Fault Tolerance****: Adaptive routing algorithms can reroute data packets around network failures, which enhances network availability and reliability.
	- ****Better Performance****: Adaptive routing algorithms can provide better network performance by selecting the shortest or the least congested path for the data packets.
	
	#### ****Disadvantages of Adaptive Routing Algorithms****
	
	- ****Complexity:**** Adaptive routing algorithms are more complex than non-adaptive algorithms, which makes them harder to implement and maintain.
	- ****Overhead:**** Adaptive routing algorithms require more processing power and memory to execute, which can lead to increased overhead and resource utilization.
	- ****Routing Loops:**** Adaptive routing algorithms may sometimes result in routing loops, which can cause data packets to be stuck in the network indefinitely.
	- ****Delay****: Adaptive routing algorithms may introduce additional delay in the network due to the time required to calculate the best path for each data packet.
	
	####****Advantages of Non-Adaptive Routing Algorithms****
	
	- ****Simplicity****: Non-adaptive routing algorithms are simple to implement and maintain, which reduces the cost and complexity of the network infrastructure.
	- ****Low Overhead:**** Non-adaptive routing algorithms require minimal processing power and memory to execute, which reduces the overhead and resource utilization.
	- ****Avoid Routing Loops****: Non-adaptive routing algorithms are less likely to result in routing loops, which reduces the chances of data packets being stuck in the network indefinitely.
	- ****Fast****: Non-adaptive routing algorithms can provide faster routing decisions since they do not require the calculation of the best path for each data packet.
	
	## ****Disadvantages of Non-Adaptive Routing Algorithms****
	
	- ****Inefficient****: Non-adaptive routing algorithms may select suboptimal paths for the data packets, which can result in congestion, longer latency, and reduced [throughput](https://www.geeksforgeeks.org/difference-between-bandwidth-and-throughput/).
	- ****Inflexible****: Non-adaptive routing algorithms cannot adjust to changing network conditions, which may result in network failures, reduced performance, and increased latency.
	- ****Unresponsive:**** Non-adaptive routing algorithms cannot respond to network faults, which may result in data packet loss and reduced network availability.
	- ****Uneven Traffic Distribution:**** Non-adaptive routing algorithms may lead to uneven traffic distribution, which may result in some links being underutilized while others are congested.

- **Repeater**: A repeater is placed between these two computers. When signal becomes weak, repeater makes it strong such that it reaches to the destination without any difficulty

- **Cables**: Computer network can be established thorough wires. The wire connects a computer to another computer or to the central device. There might be wireless network or mixture of wire and wireless connection. In wired computer network, different types of cables are being used to carry the signal from one point to another. The form of signal depends upon the type of wire is used.
	- Coaxial Cables
	- Twisted Pairs
	- Fiber Optics.
- **Network Interface Card: It is a device which makes interface between computer and rest of the network. A network cable is inserted into the NIC. NIC prepares the frame as per the format, sends and receives the data. It controls the flow between sender and receiver such that no data loss occurs



