# Ports

Port Number is a 16-bit number. Total port numbers possible are 2<sup>16</sup> = 65536. All the HTTP stuffs that we do are done on port 80.

Port Numbers from

* **0 - 1023** are already reserved for HTTP stuffs.
* **1024 - 49151** are registered for some specific applications. _Example -_ SQL runs on port **1433**.
* **49152 - 65536** can be used by you. Ports tell us which application we are working on or which application the data should go.

**Ephemeral Ports** determine which process/ instance the data will be received in the client side. Servers at most times have fixed port numbers.
