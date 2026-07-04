# Sockets

Socket is the interface between two processes for the purpose of communication. Each socket has a **specific address**. This address is composed of an **IP address and a port number**. Sockets are generally employed in **client server applications**.

### **Types of Sockets**

There are two types of Sockets:

1. **Stream Socket:** This socket establishes a reliable, connection‑oriented channel. Data is transmitted as a continuous stream, ensuring ordered delivery and error correction. This makes them ideal for applications like web servers, file transfers, and email clients where reliability is critical.
2. **Datagram Socket:** These sockets are connectionless and focus on speed rather than reliability. Each packet (datagram) is sent independently, and delivery order or integrity is not guaranteed. They are commonly used in real‑time applications such as video streaming, VoIP, and DNS queries.
3. **Raw Socket:** Raw sockets provide direct access to lower‑level network protocols, bypassing the transport layer. They allow developers to craft and inspect packets manually, which is powerful but also risky if misused.
4. **Sequenced Packet Socket (SCTP):** These sockets combine the reliability of TCP with the message‑oriented nature of UDP. They support multi‑streaming (parallel message flows) and multi‑homing (redundant network paths).

### An analogy

A **stream socket** is like a phone call. One side places the call, the other answers, you say hello to each other (SYN/ACK in TCP), and then you exchange information. Once you are done, you say goodbye (FIN/ACK in TCP). If one side doesn't hear a goodbye, they will usually call the other back since this is an unexpected event; usually the client will reconnect to the server. There is a guarantee that data will not arrive in a different order than you sent it, and there is a reasonable guarantee that data will not be damaged.

A **datagram socket** is like passing a note in class. Consider the case where you are not directly next to the person you are passing the note to; the note will travel from person to person. It may not reach its destination, and it may be modified by the time it gets there. If you pass two notes to the same person, they may arrive in an order you didn't intend, since the route the notes take through the classroom may not be the same, one person might not pass a note as fast as another, etc.

> Source: A [well-written StackOverflow answer](https://stackoverflow.com/a/4688899/19187952) to explaining the difference between the two socket types

A **raw socket** is like bypassing the steering wheel and dashboard of a car to directly manipulate the engine and gears with your hands. You gain complete control over how the vehicle runs, but it’s dangerous if you don’t know exactly what you’re doing. Similarly, raw sockets let you build and send packets exactly as you want, but misuse can break communication or expose vulnerabilities.

An **SCTP socket** is like sending several registered letters through different postal routes. Each letter is guaranteed to arrive intact, but you can send multiple letters in parallel without them interfering with each other. If one postal route is blocked, another ensures delivery. This makes communication both reliable and flexible.

### Real-life Applications

**You use a stream socket when having information in order and intact is important.** File transfer protocols are a good example here. You don't want to download some file with its contents randomly shuffled around and damaged!

**You'd use a datagram socket when order is less important than timely delivery** (think VoIP or game protocols), when you don't want the higher overhead of a stream (this is why DNS is primarily a datagram protocol, so that servers can respond to many, many requests at once very quickly), or when you don't care too much if the data ever reaches its destination.

> Source: A [well-written StackOverflow answer](https://stackoverflow.com/a/4688899/19187952) to explaining the difference between the two socket types

**Raw sockets** are used in diagnostic and security tools. For example, `ping` and `traceroute` rely on raw sockets to send ICMP packets directly. Packet sniffers like [Wireshark](https://www.wireshark.org/) use them to capture traffic for analysis. Security researchers and network engineers employ raw sockets to test firewall rules, simulate attacks, or monitor traffic patterns. They are rarely used in everyday applications because of the complexity and risks involved.

**SCTP** is widely used in telecom signaling systems, such as SS7 over IP, where reliability and multi‑streaming are essential. It’s also employed in financial transaction systems that require guaranteed delivery but benefit from parallel message streams. High‑availability servers use SCTP’s multi‑homing feature to maintain communication even if one network interface fails, ensuring continuous service.
