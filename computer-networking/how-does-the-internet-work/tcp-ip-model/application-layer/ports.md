# Ports

A **port** is a logical endpoint that helps identify which application or process should handle incoming or outgoing network data. Every port is represented by a **16‑bit number**, meaning there are 2<sup>16</sup> = 65,536 possible ports in total.

When data arrives at a device, the **IP address** identifies _where_ it should go, and the **port number** identifies _which application_ should receive it. Think of the IP address as a building’s address and the port number as the apartment number inside that building.

### Port Number Ranges

|    **Range**    | **Type**                    | **Description**                                                                      | **Examples**                                |
| :-------------: | --------------------------- | ------------------------------------------------------------------------------------ | ------------------------------------------- |
|    **0–1023**   | **Well‑known ports**        | Reserved for core system and widely used services.                                   | HTTP → 80, HTTPS → 443, FTP → 21, SSH → 22  |
|  **1024–49151** | **Registered ports**        | Assigned to specific applications by IANA (Internet Assigned Numbers Authority).     | Microsoft SQL Server → 1433, MySQL → 3306   |
| **49152–65535** | **Dynamic / Private ports** | Available for user‑defined or temporary use. Often used for client‑side connections. | Custom apps, local testing, ephemeral ports |

### Ephemeral Ports

When a client connects to a server, it temporarily uses an **ephemeral port** which is a short‑lived port number automatically assigned by the operating system.\
For example, when your browser connects to a web server on port 80 (HTTP), your computer might use port 52341 for that specific session. This helps the system track which process initiated the connection and where to send the response.

Servers typically listen on **fixed ports** (like 80 for HTTP or 443 for HTTPS), while clients use **ephemeral ports** that change with each new connection.
