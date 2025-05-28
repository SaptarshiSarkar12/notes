# Transport Layer

The transport layer is responsible for the **transportation of the data from the&#x20;**_**network**_**&#x20;to the&#x20;**_**application**_. It is located in your device. When a resource needs to be sent, it is given to the socket which gives to the transport layer multiplexer. **Multiplexer** allows us to send multiple things to multiple destinations (might be in the same device). This is called **multiplexing**. **De-multiplexer** allows us to receive multiple things from multiple destinations. This is called **demultiplexing**. De-multiplexer gives the data to the concerned socket. The Transport Layer attaches the socket port numbers to the data packets. It also takes care of congestion control using congestion control algorithms built in TCP.

### **Checksum**

A particular string value is created from the data sent. When the data is received at the other end, its checksum is calculated. As the sender has attached the checksum calculated by him in the data packets, then, if the checksums match, it's okay, else, something has gone wrong.

### **Timers**

When a data packet is sent, the timer is started in the sender's device. When the confirmation is received, the timer ends. Suppose the second packet sent gets lost, the timer once started, expires after some time. That's how you can know which data packet has been lost. This timer is known as **Retransmission timer**.

### **Sequence Numbers**

A value/number for the unique identification of data packets, is called sequence numbers. This is useful for identification of duplicate data packets at the receiver's end, if the same packet is retransmitted by the sender for not receiving the acknowledgement message for that packet.

### **Transport layer network protocols**

The protocols used in the transport layer are

#### **TCP (Transmission Control Protocol)**

TCP is a transport layer protocol that provides a **reliable stream delivery and virtual connection service to applications through the use of sequenced acknowledgement**. TCP is a **connection-oriented protocol**, as it requires a **connection to be established between applications before data transfer**. Through flow control and acknowledgement of data, **TCP provides extensive error checking**. TCP ensures **sequencing of data**, meaning the data packets arrive in order at the receiving end. **Retransmission of lost data packets is also feasible with TCP**. TCP segments (divides into chunks) the data received from the application layer and add headers to it and re-assemble and put the data received into one. Congestion in the network and error is controlled. It maintains the order of data using sequence numbers. It is bi-directional. There can be only two endpoints. It adds sequence and acknowledgement number to the data.

**3-way handshake:** The client sends a connection request to the server with a **synchronization flag** (a value added in the header) and a **sequence number** (**Random Numbers** to prevent hackers to guess the number) (Suppose, 32). The server then sends the synchronization flag (as it is a new connection), **acknowledgement flag** and acknowledgement number (1 added to the previous sequence number, here, 32 + 1 = 33) along with the new **sequence number** (Suppose, 56) generated after some mathematical operations done on the previous sequence number. Client then sends the **Acknowledgement flag** along with the new sequence number (1 added to the first sequence number sent by it, here, 32 + 1 = 33) and the acknowledgement number (1 added to the previous sequence number, here, 56 + 1 = 57). Then, the connection is established. There are other flags like reset and finish.

**Advantages:**

* TCP ensures three things: data reaches the destination, reaches it on time, and reaches it without duplication.
* TCP automatically breaks data into packets before transmission.

**Disadvantage:**\
TCP cannot be used for broadcast and multicast connections.

#### **UDP (User Datagram Protocol)**

UDP is a **connection-less protocol** that provides a **simple but unreliable message service**. Unlike TCP, UDP adds **NO reliability, flow control, or error recovery functions**. UDP is useful in situations where the reliability mechanisms of TCP are not necessary. Retransmission of lost data packets **isn't possible** with UDP. Here, data _**may or may not be delivered, may change and may not be in order.**_ UDP uses a checksum to detect whether the data has been corrupted, but it does not attempt to correct any errors.

One UDP packet contains the **data (65536 bytes)** along with the headers containing the **source and destination port numbers (2 + 2 = 4 bytes), length of the datagram (2 bytes) and the checksum (2 bytes)**.

_Uses of UDP_ - Video Conference, DNS and gaming.

**Advantages:**

* Broadcast and multicast connections are possible with UDP.
* UDP is faster than TCP.

**Disadvantages:**

* In UDP, it's possible that a packet may not be delivered, be delivered twice, or not be delivered at all.
* Manual disintegration of data packets is needed.
