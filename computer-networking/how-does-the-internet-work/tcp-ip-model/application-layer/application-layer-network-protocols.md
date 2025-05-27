# Application Layer Network Protocols

Protocols are set of rules used on the internet. The Protocols which are commonly used in the Application Layer are given below.

### **DNS (Domain Name System protocol)**

The DNS protocol helps in **translating or mapping host names to IP addresses**. DNS works on a **client-server model** and uses a **distributed database** over a hierarchy of name servers. When we visit a website for the first time, the IP Address of the website is stored in the local cache. Suppose the IP Address is not found in the local cache, then it will be looked in the local DNS Server (ISP has all info about all websites you visit even if in incognito mode) which is the first point of contact. If the IP Address is not found there, it will be looked for in the root server and if not found even, it will be looked in the top-level domain. After getting the IP, the website server is connected.\
**Classes of Domains**

<figure><img src="https://camo.githubusercontent.com/5859ba78748416e268ef2752c4c1724bf66109e5b22af812bb3660d506107c73/68747470733a2f2f73656172636866616374732e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031392f30372f646f6d61696e2d6e616d652d70617274732e706e67" alt="" width="375"><figcaption><p>Parts of Domain Name</p></figcaption></figure>

* **Top-level domain** - Root DNS Servers. They have top-level domains like .io, .org, .com, etc. The authorities maintaining this root DNS server can be seen in this website - [Root-servers.org](https://root-servers.org/). The top-level domains are registered by [ICANN](https://www.icann.org/) (The Internet Corporation for Assigned Names and Numbers).
* **Second level Domain** - The top-level domains themselves have domains like student.io, commclassroom.org, google.com, etc.

Hosts are identified based on their IP addresses, but memorizing an IP address is difficult due to its complexity. IPs are also dynamic, making it all the more necessary to map domain names to IP addresses. DNS helps resolve this issue by **converting the domain names of websites into numerical IP addresses**.

**Advantages:**

* DNS facilitates internet access.
* Eliminates the need to memorize IP addresses.

**Disadvantages:**

* DNS queries don't carry information pertaining to the client who initiated it. This is because the DNS server only sees the IP from where the query came from, making the server susceptible to manipulation from hackers.
* DNS root servers, if compromised, could enable hackers to redirect to other pages for phishing data.

### **FTP (File Transfer Protocol)**

File Transfer Protocol enables **file sharing between hosts, both local and remote**, and **runs on top of TCP**. For file transfer, FTP **creates two TCP connections: control and data connection**.&#x20;

The control connection is used to **transfer control information like passwords, commands to retrieve and store files, etc.**, and the data connection is used to **transfer the actual file**. Both of these connections run in **parallel** during the entire file transfer process.

**Advantages:**

* Enables sharing large files and multiple directories at the same time.
* Allows you to resume file sharing if it was interrupted.
* Lost data can be recovered, and file transfer can be scheduled.

**Disadvantages:**

* FTP lacks security. Data, usernames, and passwords are transferred in plain text, making them vulnerable to malicious actors.
* FTP lacks encryption capabilities, making it non-compliant with industry standards.

### HTTP (Hyper Text Transfer Protocol)

HTTP is an application layer protocol used for **distributed, collaborative, and hypermedia information systems**. It works on a **client-server model**, where the web browser acts as the client. Data such as text, images, and other multimedia files are shared over the World Wide Web using HTTP. As a request and response type protocol, the client sends a request to the server, which is then processed by the server before sending a response back to the client.

HTTP is a **stateless protocol**, meaning the client and server are only aware of each other while the connection between them is intact. After that, both the client and server forget about each other's existence. Due to this phenomenon, both the client and the server **can't retain information between requests**.

**HTTP Methods** - This tells the servers what to do.

* **GET**: Requesting a data.
* **POST**: Giving something to the server, like form data.
* **PUT**: Puts data at a specific location in the server.
* **DELETE**: It deletes a resource on the server.

**Status Code** - Status Code tells what happened to our request.

* 1XX → Informational.
* 2XX → Success codes.
* 3XX → Redirection purposes.
* 4XX → Client error.
* 5XX → Server error.

**Cookies** - It is a file containing unique string stored in the client's browser. When a website is visited first, a cookie is set. Next time, whenever a new request is made to that website, the cookie will be set in the request headers.\
Third-party cookies are those cookies that are set while navigating to the external URLs that you don't know.

**Advantages:**

* Memory usage and CPU usage are low because of lesser concurrent connections.
* Errors can be reported without closing connections.
* Owing to lesser TCP connections, network congestion is reduced.

**Disadvantages:**

* HTTP lacks encryption capabilities, making it less secure.
* HTTP requires more power to establish communication and transfer data.

### IMAP and IMAP4 (Internet Message Access Protocol (version 4))

IMAP is an **email protocol** that lets end users **access and manipulate messages** stored on a mail server from their email client as if they were present locally on their remote device. IMAP follows a **client-server model**, and **lets multiple clients access messages on a common mail server concurrently**. IMAP includes **operations for creating, deleting, and renaming mailboxes; checking for new messages; permanently removing messages; setting and removing flags**; and much more. The current version of IMAP is version 4 revision 1.

**Advantages:**

* As the emails are stored on the mail server, local storage utilization is minimal.
* In case of accidental deletion of emails or data, it is always possible to retrieve them as they are stored on the mail server.

**Disadvantages:**

* Emails won't work without an active internet connection.
* High utilization of emails by end users requires more mailbox storage, thereby augmenting costs.

### POP and POP3 (Post Office Protocol (version 3))

The Post Office Protocol is also **an email protocol**. Using this protocol, the end user can **download emails from the mail server to their own email client**. Once the emails are downloaded locally, they **can be read without an internet connection**. Also, **once the emails are moved locally, they get deleted from the mail server, freeing up space**. POP3 is **NOT designed to perform extensive manipulations with the messages on the mail server, unlike IMAP4**. POP3 is the latest version of the Post Office Protocol.

**Advantages:**

* Read emails on local devices without internet connection.
* The mail server need not have high storage capacity, as the emails get deleted when they're moved locally.

**Disadvantages:**

* If the local device on which the emails were downloaded crashes or gets stolen, the emails are lost.
* Email folders can become corrupted, potentially losing the entire mailbox at once.

### SMTP (Simple Mail Transfer Protocol)

SMTP is a protocol designed to **transfer electronic mail reliably and efficiently**. SMTP is a **push protocol** and is used to **send the email**, whereas **POP and IMAP are used to retrieve emails on the end user's side**. SMTP **transfers emails between systems, and notifies on incoming emails**. _**Using SMTP, a client can transfer an email to another client on the same network or another network through a relay or gateway access available to both networks**_.

#### How E-Mail works?

For sending e-mail, SMTP protocol is used.\
Sender sends the e-mail to the sender's SMTP server. The e-mail stays there for a while, then the sender's server connects to the receiver's SMTP server. This happens only when the sender and receiver are not using the same e-mail platform like only google, or only yahoo, etc. When the receiver logs in to the receiver's client, the e-mail from the receiver's server is downloaded into the client which the receiver can view. For receiving e-mails, POP (Post Office Protocol) protocol is used. At first, the client authorizes with the receiver's POP server and then transact the e-mails. Later, the e-mails are updated. The folders like sent items and draft folder are NOT downloaded by POP.

**Advantages:**

* Ease of installation.
* Connects to any system without any restriction.
* It doesn't need any development from your side.

**Disadvantages:**

* Back and forth conversations between servers can delay sending a message, and also increases the chance of the message not being delivered.
* Certain firewalls can block the ports used with SMTP.

### Telnet (Terminal emulation protocol)

Telnet is an application layer protocol that enables a user to **communicate with a remote device**. A Telnet client is installed on the user's machine, which **accesses the command line interface of another remote machine that runs a Telnet server program**.

Telnet is mostly used by **network administrators to access and manage remote devices**. To access a remote device, a network admin needs to enter the **IP or host name of the remote device**, after which they will be presented with a **virtual terminal that can interact with the host**.

**Advantages :**

* Compatible with multiple operating systems.
* Saves a lot of time due to its swift connectivity with remote devices.

**Disadvantages :**

* Telnet lacks encryption capabilities and sends across critical information in clear text, making it easier for malicious actors.
* Expensive due to slow typing speeds.

### SNMP (Simple Network Management Protocol)

SNMP is an application layer protocol used to **manage nodes, like servers, workstations, routers, switches**, etc., on an IP network. SNMP enables network admins to **monitor network performance, identify network glitches, and troubleshoot them**. SNMP protocol is comprised of three components: a **managed device**, an **SNMP agent**, and an **SNMP manager**.

The SNMP agent resides on the **managed device**. The agent is a **software module** that has local knowledge of management information, and **translates that information into a form compatible with the SNMP manager**. The SNMP manager presents the data obtained from the SNMP agent, helping network admins **manage nodes effectively**.

Currently, there are **three versions** of SNMP: SNMP **v1**, SNMP **v2**, and SNMP **v3**. Both versions 1 and 2 have many features in common, but SNMP v2 offers enhancements such as additional protocol operations. **SNMP version 3 (SNMP v3) adds security and remote configuration capabilities** to the previous versions.
