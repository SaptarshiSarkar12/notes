# Network Topologies

Network topology is a fundamental concept in computer networking that describes the structured layout—either physical or logical—of interconnected nodes and the pathways for data transmission between them. Here are the different kinds of network topologies commonly used:

### **Bus Topology**

Bus topology is a network type in which every computer and network device is connected to a single cable.\
**Advantages:**

* If N devices are connected to each other in a bus topology, then the number of cables required to connect them is 1, which is known as backbone cable, and N drop lines are required.
* The cost of the cable is less as compared to other topologies, but it is used to build small networks.

**Limitations:**

* If the cable fails, the whole network crashes.
* Only **one person** can send data at a time.
* Data is transmitted from one end to another end in a **single direction**.
* If the network traffic is heavy, it increases collisions in the network. To avoid this, various protocols are used in the MAC layer known as Pure Aloha, Slotted Aloha, CSMA/CD, etc.

<figure><img src="../../.gitbook/assets/bus-topology-diagram-29007878.jpg" alt="Bus Topology Diagram" width="563"><figcaption><p>Bus Topology Diagram</p></figcaption></figure>

### **Ring Topology**

Ring Topology is a network type in which each computer is connected to the next in a circular way.\
**Advantages:**

* The possibility of collision is minimum in this type of topology.
* Cheap to install and expand.

**Limitations:**

* If one of the cable breaks, then the whole network crashes.
* Lot of unnecessary calls are made.

![Ring Topology Diagram](../../.gitbook/assets/ring-topology.jpg)

### **Star Topology**

The star topology is a network type in which all computers are connected through a central device.\
**Advantages:**

* Star topology systems are highly scalable.
* Multiple devices can be connected through the star topology.

**Limitations:**

* If the central device fails, the whole network will crash.
* Performance is based on the central device.
* Star topology is very expensive to install.

<figure><img src="../../.gitbook/assets/Star Topology.jpg" alt="Star Topology Diagram" width="473"><figcaption><p>Star Topology Diagram</p></figcaption></figure>

### **Tree Topology**

The Tree Topology is a network type where many star topologies are connected using a bus topology.\
**Advantages:**

* It allows more devices to be attached to a single central hub thus it decreases the distance that is traveled by the signal to come to the devices.
* It has higher [fault tolerance](https://en.wikipedia.org/wiki/Fault_tolerance).

**Limitations:**

* A tree topology relies heavily on its main bus cable.
* The installation of a tree topology is difficult.

![Tree Topology Diagram](../../.gitbook/assets/dc-lec03-topologies-34-638.jpg)

### **Mesh Topology**

The Mesh Topology is a network type where each and every computers are connected to each other.\
**Advantages:**

* Failure of one single device does not affect the network.
* Adding new devices does not affect data transmission.

**Limitations:**

* Expensive.
* Time-consuming to build and maintain.
* High risk of redundant connection.

![Mesh Topology Diagram](../../.gitbook/assets/mesh-topology-1-696x348.jpg)
