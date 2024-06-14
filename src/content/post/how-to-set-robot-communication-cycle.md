---
title: "How to set robot communication cycle?"
publishDate: "07 Jun 2024"
description: "--------------------------------------------------"
tags: ["SW", "ROS", "ROS2", "robotics", "software development"]
---

Q. I have a question when we communicate with a robot. The cycle changes from 2ms to 3ms or 5ms while socket programming with the robot. How do people usually set the communication cycle regularly?

<br>

A. You have to match it with the robot's embedded board clock. If it's a PC, you have to use the RT kernel.

<br>

RT kernel : PreemptRT (soft real time), Xenomai (hard real time)

<br>
<br>
<br>

![7](@/assets/7.jpeg)