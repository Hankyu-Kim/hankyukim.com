---
title: "TCP Flow Control"
publishDate: "12 Jun 2024"
description: "--------------------------------------------------"
tags: ["TCP", "flow-control"]
---

Flow control is a method that clients (RX) use to fix ‘overflow’ issues caused by the difference in data processing times between the server (TX) and the client (RX).

There's no problem at all if the receiver’s data processing time is faster than the sender’s. However, problems can arise if the receiver’s data processing time is slower than the sender’s.

1. **Stop and Wait**
    

The server (TX) sends a piece of data and then pauses, waiting to receive confirmation from the client (RX) that the data has been received.

2. **Sliding Window**
    

Overflow can be prevented by setting the server’s sending window (awnd) to be smaller than the client’s receiving window (rwnd), as this ensures that the amount sent is less than the amount received. If the receiver communicates the size of their receiving window (rwnd) back to the sender as feedback, the sender can then adjust their sending window (awnd) to be smaller than the receiver’s window (rwnd).

![6](@/assets/6.jpeg)