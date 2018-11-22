---
layout: project
type: project
image: images/time.png
title: Daytime Server
permalink: projects/DaytimeServer
date: 2018
labels:
  - Networking
  - Sockets Programming
  - C
summary: Daytime Server implementation in C.
---

<img class="ui medium centered rounded image" src="/images/time.png">

This project was a simple exercise to become familiar with using the C sockets library. The server configures and listens on a socket on the port specified by the arguments. The server will respond to all connections with an ASCII character string of the current date and time. This server can be tested by running the server on port 13 (daytime port) and then connecting to the server using telnet with the server's IP address and the daytime protocol specified.

Here is an example of the daytime server being tested with telnet.
Server terminal:
```
$ make
gcc -pedantic-errors -Wall -c server.c
gcc -o server server.o
$ ./server 13
```

Client terminal:
```
$ telnet localhost daytime
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
2018/11/21 15:17:42
Connection closed by foreign host.
```
