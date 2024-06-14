---
title: "QoS Parameter from DDS"
publishDate: "11 Jun 2024"
description: "--------------------------------------------------"
tags: ["DDS", "QoS", "ROS2"]
---

1. History : Select length of que, FIFO/LIFO.
    
2. Reliability : Using ACK/NACK signal for reliability.
    
3. Durability : Remove history of sent data.
    
4. Deadline : Get noticed from the latency delay.
    
5. TimeBasedFilter : Limit 'subscribe' for once in a certain time.
    
6. DestinaitonOrder :
    

* SOURCE\_TIMESTAMP : Sort data based on data published time.
    
* RECEPTION\_TIMESTAMP : Sort data based on data subscribed time.
    

7. Lifespan : Set the data lifespan.
    
8. Liveliness : Using AUTO/MANUAL signal to manage liveliness.
    
9. Partition : Categorize by partition name (only communicat with same group's DDS object).
    
10. Ownership :
    

* SHARED : Share the data simultaneously.
    
* EXCLUSIVE : Receive only data based on priority