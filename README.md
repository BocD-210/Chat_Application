# CHAT APPLICATION

## Overview.

This is a mini project when i completed the **Linux Programming** course. The Chat Application is a **peer to peer(P2P)** chat system implemented in C for the Embedded System. This designed to demonstrate fundamental concepts of network programming the application enables multiple instances to communicate seamlessly over a **TCP/IP network**. This project highlights practical aspects of Linux-based systems programming, combining networking, process synchronization, and memory management into a functional and extendable communication tool.

## Key Features.

- **Multithreading:** Uses POSIX threads (`pthread`) to handle multiple clients concurrently.
- **Command-Line Interface (CLI):** Provides a simple CLI for user interaction such as `help` , `show my port` , `send` , `terminate` , `exit`.
- **Connection Management:** To list active connections, send messages, and terminate connections.
- **Debugging and memory safety:** ensured through the use of `Valgrind tool` for detecting memory leaks.
-  Implementation of **TCP sockets** and **inter-process communication (IPC)** for efficient message exchange.

This will used the Multithreading to handle the multiple client connection, and have some command line interface , connection managerment to list active the connection and send messages and terminalted the connection
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

## Illustrate about the chat application's interface.

**Video demo of the project result** : [Google Driver Link](https://drive.google.com/file/d/1doIcjdHaZTqoYTeZRaZu9PbJDvzgueHc/view?usp=sharing) .

![Diagram](Interface%20Chat%20App.png)

When you run the app successful! The GUI of App will like this image and after the `>>`, let's choose a `CLI` to enjoy the app

Some command line interface in the app such as: 
- `help` and `myport`: It's will show manual and the port you chosen.
- `connect <destination> <port>`: when you use this CLI, you need to know the destination you want to connect (The destination is the **IP Address** of the chat app run) and port is **Number Port** you chosen.
- `list`: When you connect with client successfully, this client will allocated a **ID**, This ID very helpful for the connection manager. And this ID used to terminate the connection.
- `terminate <connection ID>`: You need to know the connection ID you want to terminate, and then the connection between you and this will stop.
- `send <connection ID> <message>` : Used to send message to the clients (You need to have the **connection ID** if you want to use this CLI).
- `exit`: This CLI will terminate all the connection was connected, and then the application will end.

While you build and run the project, you can use the `Valgrind tool` to check the memory leak (I think **Memory Leak** is a big issues in the **Embedded Major**).
This is the result when i check the memory leak by **Valgrind tool** in my project.

```
==14412== HEAP SUMMARY:
==14412==     in use at exit: 0 bytes in 0 blocks
==14412==   total heap usage: 10 allocs, 10 frees, 6,422 bytes allocated
==14412== 
==14412== All heap blocks were freed -- no leaks are possible
==14412== 
==14412== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
```
**NOTE:** You need to clean the project when you end the chat app, advoid some problems related to such as memory overflow when you allocated.

```bash
make clean
```

## Workspace Structure.
```
.
├── inc
│   ├── command.h
│   ├── connection.h
│   ├── server.h
│   ├── socket.h
│   └── types.h
├── Makefile
├── src
│   ├── command.c
│   ├── connection.c
│   ├── main.c
│   ├── server.c
│   └── socket.c
└── valgrind-out.txt
```

## Contact

For issues or inquiries, open a GitHub issue or contact [bocdo210@gmail.com].
