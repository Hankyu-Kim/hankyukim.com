---
title: "Multicast VS Broadcast"
publishDate: "13 Jun 2024"
description: "--------------------------------------------------"
tags: ["Network"]
---

### Multicast

A router allows numerous hosts to receive data, even if they are far away. In other words, regardless of how many hosts are registered or where they are located, you can simply set up the multicast group and send the packet once. This way, a single multicast packet is duplicated and delivered to all the recipients with the router's assistance.

### Routing and TTL (Time To Live)

To send a multicast packet, you need to configure its TTL. TTL stands for Time To Live and determines how far the packet will travel. It is an integer value that decreases with each router hop, and the packet is discarded when TTL reaches 0.

---

### Broadcast

Unlike multicast, which can send packets to hosts in different networks as long as they are part of the multicast group, broadcast is limited to sending packets to hosts within the same network.

### Directed Broadcast and Local Broadcast

For example, in a Class C network, to send a packet to all hosts in the network starting with 192.12.34, you would use the IP address 192.12.34.255. This specific targeting of a network is known as 'directed broadcast'.

Additionally, the IP address 255.255.255.255 is reserved for local network broadcasts. If a host on the 192.32.32.0 network sends a packet to 255.255.255.255, all hosts connected to the 192.32.32.0 network will receive it. Using the 255.255.255.255 address to broadcast packets to all hosts within the same network as the sender is referred to as a 'local broadcast'.