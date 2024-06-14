---
title: "blocking VS non blocking"
publishDate: "14 Jun 2024"
description: "--------------------------------------------------"
tags: ["Network"]
---

### Blocking

In a blocking scenario, a thread remains idle while it waits for a method call to complete its request to a device.

#### Blocking Socket

When the receive buffer is full, the TCP sender's `send()` method becomes blocked, halting communication even though the connection is still active. Similarly, if the receive buffer is empty, the receiver's `recv()` method will also block until at least one datagram is recieved.

![14_1](@/assets/14_1.png)

**Cons:** In a blocking socket setup, you need a separate thread for each network host. Each thread is responsible for data transfer with its designated network host. This approach works well with a small number of connections. However, as the number of connected hosts increases, it requires significantly more memory since each thread’s call stack typically consumes about 1 MB. Additionally, frequent context switching between threads can further degrade performance.

### Non-Blocking Socket

Non-blocking sockets, supported by the operating system, allow for more efficient resource use by avoiding the blocking of socket methods. These sockets return immediately when a method is called.

In a non-blocking socket, if the buffer has data, it is retrieved and returned immediately. If the buffer is empty, the method returns a "would block" error code, indicating that the operation cannot be completed at the moment.

In conclusion, non-blocking sockets can handle a large number of socket operations without delays, making them ideal for scenarios where high throughput and minimal latency are critical.

![14_1](@/assets/14_2.png)

The problem with this non block socket is that if the socket continues to be in a would block state, it will continue to loop that can cause a single CPU core in 100 percentage usage.  
  
To solve this problem, if there is a single change in the state of one of numerous sockets being a would block, a function that informs the situation that resolves the CPU usage congestion is needed.  
  
The function that does this is select() or poll.  
If select is called, it returns immediately if there is even one socket capable of I/O processing.  
Otherwise block up to 100 milliseconds.