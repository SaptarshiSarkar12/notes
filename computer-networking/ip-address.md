# IP Address

Every device which can connect to each other, have their own IP Addresses. It is in the format of " **X.X.X.X** ". Every single "**X**" can have values from _0_ to _255._

When you type [google.com](https://www.google.com/) in the address bar of your browser, it resolves to the IP address of Google.

To get your system's IP Address, run -

1.  For **Windows System** :

    ```sh
     ipconfig
    ```

    in the **command prompt**.
2.  For **Mac and Linux/Unix Systems** :

    ```
    curl ifconfig.me
    ```

    in the **terminal**.

**Internet Service Provider** (_ISP_) gives you a modem/router which has a global IP Address. The modem will give IP Addresses to each of the device connected to it using the DHCP (Dynamic Host Configuration Protocol). Those IP Addresses are called **Local IP Addresses**.

When we send request (type the website link in the browser address bar) a server (Google server in this case), it can see the **global IP Address** and **not** the _Local IP Address_. The server sends the response and the modem/router decides which device to send back the response, using **NAT (Network Address Translation) Protocol**. **IP Address** decides which _device_ to send the data and **Port Number** determines which application requested the data.
