---
title: "Sync VS Async"
publishDate: "18 Jun 2024"
description: "--------------------------------------------------"
tags: ["Network"]
---

#### Synchronous

The term "synchronous" means things happening at the same time.

Imagine a scenario where you send a message to a server saying, "I just got connected." The server takes a moment and then responds, "Oh, really? You just got connected! I'll let everyone know."

In this case, your client (you) has to wait for the server's response before doing anything else. This is what we call synchronous communication — you're waiting for both the request and the response to happen one after the other, almost simultaneously.

Let's look at another example: You’re calling your team leader. If they don’t pick up immediately, you hold the phone until they answer. During this wait, you can’t do anything else because you're focused on that call.

In programming terms, this means that the client (your program) is effectively "paused" until the server responds. The client request and server response are tightly linked in time.

#### Asynchronous

On the other hand, "asynchronous" means things do not occur at the same time.

Let's say you call your team leader again, but this time, instead of waiting, you switch your phone to speaker mode and start playing a game while waiting for them to pick up. Here, you're not just waiting; you’re doing something else while the phone call is pending.

In an asynchronous program, after the client sends a request to the server, it doesn't wait for the response before doing other tasks. The client can continue with its other work and handle the server's response whenever it comes. This way, the client isn’t "paused" and can multitask effectively.

One might think, “Isn’t asynchronous always better than synchronous?” Not necessarily. Each approach has its own use cases and benefits.

#### Blocking

"Blocking" means halting a program’s execution until an operation is completed.

In synchronous programming, blocking occurs because the program waits for a response before moving on. Using the phone example, you can’t do anything else until your team leader picks up the phone.

When we use socket libraries in programming, the default behavior is blocking. For example, when you use `send` or `recv` methods, the program waits until it gets a response before continuing.

#### Non-blocking

"Non-blocking" means not halting the program's execution even if an operation isn’t completed yet.

In non-blocking scenarios, the program can continue to run other tasks while it waits for a response. Going back to our example, you switch your phone to speaker mode and play a game while waiting for your team leader to answer. You’re not stopped by the wait.

In programming, making sockets non-blocking (using methods like `fcntl`) allows the `send` and `recv` operations to return immediately, regardless of whether they have data to process. If there's no immediate data, the status is recorded, and the program can decide what to do next based on this status.

Understanding these concepts helps you decide when to use each method based on your application's needs.