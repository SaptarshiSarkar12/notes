# Data Link Layer

The data link layer is responsible for sending the data packets received from the network layer, over a physical layer. Router attaches the correct private IP Address to the data packets received, ensuring that the data receives the correct destination.

### **DHCP (Dynamic Host Configuration Protocol)**

DHCP is a **communication protocol** that enables network administrators to **automate the assignment of IP addresses** in a network. The DHCP server is a pool of IP Addresses, and it assigns IP Addresses to the devices connected.

In an IP network, every device connecting to the internet requires a unique IP. DHCP lets network admins distribute IP addresses from a central point and automatically send a new IP address when a device is plugged in from a different place in the network. DHCP works on a **client-server model**.

**Advantages:**

* Centralized management of IP addresses.
* Seamless addition of new clients into a network.
* Reuse of IP addresses, reducing the total number of IP addresses required.

**Disadvantages:**

* Tracking internet activity becomes tedious, as the same device can have multiple IP addresses over a period of time.
* Computers with DHCP cannot be used as servers, as their IPs change over time.

### **Data Link Layer Address or MAC Address**

MAC Address depends on the network interface. Two computers at the data link layer communicate with each other using the data link layer address, might happen manually or automatically. ARP (Address Resolution Protocol) cache is used to find out the data link layer address. the frames (Data link layer address of sender and IP Address of destination along with the data) are sent to all the devices connected to the same network.

### **Data Link Layer Protocols**

The protocols used in data link layer are:

#### **ARP (Address Resolution Protocol)**

The Address Resolution Protocol helps **map IP addresses to physical machine addresses (or a MAC address for Ethernet) recognized in the local network**. A table called an **ARP cache is used to maintain a correlation between each IP address and its corresponding MAC address**. _**ARP offers the rules to make these correlations and helps convert addresses in both directions.**_

**Advantage:**

MAC addresses need not be known or memorized, as the ARP cache contains all the MAC addresses and maps them automatically with IPs.

**Disadvantages:**

* ARP is susceptible to security attacks called ARP spoofing attacks.
* When using ARP, sometimes a hacker might be able to stop the traffic altogether. This is also known as ARP denial-of-services.

#### **SLIP (Serial Line IP)**

SLIP is used for **point-to-point serial connections using TCP/IP**. SLIP is used on **dedicated serial links**, and sometimes for **dial-up purposes**. SLIP is useful for **allowing mixes of hosts and routers to communicate with one another**; for example, **host-host, host-router, and router-router** are all common SLIP network configurations. SLIP is merely a **packet framing protocol**: It defines a **sequence of characters that frame IP packets on a serial line**. It does **NOT provide addressing, packet type identification, error detection or correction, or compression mechanisms.**

**Advantages:**

* Since it has a small overhead, it is suitable for usage in microcontrollers.
* It reuses existing dial-up connections and telephone lines.
* It's easy to deploy since it's based on the Internet Protocol.

**Disadvantages:**

* SLIP doesn't support automatic setup of network connections in multiple OSI layers at the same time.
* SLIP does not support synchronous connections, such as a connection created through the internet from a modem to an internet service provider (ISP).
