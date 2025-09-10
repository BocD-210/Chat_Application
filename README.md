# CHAT APPLICATION

## Overview.

This is a mini project when i completed the **Linux Programming** course. The Chat Application is a **peer to peer(P2P)** chat system implemented in C for the Embedded System. This designed to demonstrate fundamental concepts of network programming the application enables multiple instances to communicate seamlessly over a **TCP/IP network**. This project highlights practical aspects of Linux-based systems programming, combining networking, process synchronization, and memory management into a functional and extendable communication tool.

## Key Features.

- **Multithreading:** Uses POSIX threads (`pthread`) to handle multiple clients concurrently.
- **Command-Line Interface (CLI):** Provides a simple CLI for user interaction such as `help` , `show my port` , `send` , `terminate` , `exit`.
- **Connection Management:** To list active connections, send messages, and terminate connections.
- **Debugging and memory safety:** ensured through the use of `Valgrind tool` for detecting memory leaks.
-  Implementation of **TCP sockets** and **inter-process communication (IPC)** for efficient message exchange.

## Installation.

### 1. Clone the repository

```bash
git clone https://github.com/BocD-210/Chat_Application.git
cd Chat_Application
```

### 2. Build project and run the application.

```bash
make
```

After you built the project completely, you need to choose a `port number` for your application (this number is a destination to connect with another client). and run the application with this port


```bash
Example:
./chat_app 4000
```

And then you can run the app with another port then you can communication.

### Illustrate about the chat application's interface.


