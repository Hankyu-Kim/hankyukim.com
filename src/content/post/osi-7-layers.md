---
title: "OSI 7 layers"
publishDate: "06 Jun 2024"
description: "--------------------------------------------------"
tags: ["Network"]
---

\[7\] Application Layer data unit : message protocol : HTTP, SMTP, FTP, SIP, etc. As the final destination, application layer is commonly used for the multiple applications to communicate with each other. It is closest to the users, often interacting directly through web browsers or applications. Various protocol exists at this layer, and new ones can be easily added.

<br>

\[6\] Presentation Layer data unit : message protocol : ASCII, MPEG, etc. Presentation Layer handles the encoding or decoding the data exchanged at the application layer. (e.g., converting ASCII to UTF-8) It translate data decided the application and the network formats. This layer isn't part of the internet layer and must be supported by the application layer or developed by application developers.

<br>

\[5\] Session Layer data unit : message protocol : NetBIOS, TLS, etc. Session Layer manages the opening, closing and managing of sessions between end-user application processes. If a disconnection occurs, its protocols attempt to restore the connection. If there is no connection for a long period, the protocol closes and can resume the connection. It allows for either simultaneous (full-duplex) or alternate (half-duplex) data transmission while receiving data. This layer is not part of the internet layer and needs supports from the application layer or application developers.

<br>

\[4\] Transport Layer data unit : message protocol : TCP, UDP, SCTP, etc. Transport Layer carries message from the upper layers to the lower layers. It manages errors and, if a message is too large, it segments it before passing it to Network Layer. TCP, which is connection-oriented, and UDP, which is connectionless, are commonly used protocols.

<br>

\[3\] Network Layer data unit : datagram, packet, etc. protocol : IP, ICMP, ARP, RIP, BGP, etc. Network Layer routes packets from host to host. often through multiple routers. It creates packets using destination address from Transport Layer and delivers them to the destination's Transport Layer. In the context of the Internet, the IP protocol is the primary example.

<br>

\[2\] Data Link Layer data unit : frame protocol : PPP, Ethernet, Token ring, IEE 802.11(Wifi), etc. This layer is responsible for transferring data between nodes on a network segment across the physical layer. It provides the means to transfer data between network entities and may also detect and correct errors from the physical layer. Ethernet protocol is representitive protocol, transferring frames between nodes using MAC address. i.e. Bridge, Switch HUB

<br>

\[1\] Physical Layer data unit : bit protocol : DSL, ISDN, etc. Pyhisical Layer transmit electrical signals between devices, moving each bit of the data frame between nodes. Ethernet includes serveral Physical Layer protocol. i.e. Repeater

<br><br><br>

![6](@/assets/6.jpeg)