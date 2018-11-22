---
layout: project
type: project
image: images/routing.png
title: Simple Router
permalink: projects/SimpleRouter
date: 2018
labels:
  - Networking
  - C
summary: I implemented a simplified version of a router that forwards packets using a routing protocol similar to Distance Vector
---

<img class="ui large centered rounded image" src="/images/routing.png">

<h2>What does a router do?</h2>
Before explaining what my program does, I decided to first briefly explain about the purpose of a router. The most basic explanation for what a router does is: a router forwards packets of data between a sender and a receiver. Routers are used to forward packets of data between different subnets and without them, the Internet would not exist. A router needs to have a way of knowing the possible routes a packet could take. The information on routes is usually stored in a routing table within the router. Different routing protocols describe how to determine the best route and how to exchange information on routes between connected routers.

<h2>Summary of my Implementation</h2>
The router is started by giving it a list of interface addresses as command line arguments and information on the simulated interfaces as a `simconfig` file. The router then opens simulated SLIP (Serial Line Internet Protocol) interfaces for each of the interface addresses specified in the arguments. A static routing table is built with entries for the router's own interfaces. The router is then free to receive routing packets or packets to forward to other routers. Whenever a routing packet is received (addressed to the router), the router will compare its contents with its routing table and update the routes as necessary. Routing packets are broadcast to all interfaces every 30 seconds. If the packet a router receives is not addressed to the router but a route is available, the router will perform IP processing on that packet and forward it. This router uses IPv6.

<h2>SLIP</h2>
All of the data that a router sends or receives is done over a simulated SLIP (Serial Line Internet Protocol) connection. I did not implement the SLIP simulation, it was provided for this project. Because the SLIP implementation runs on UDP, it needs information to configure the UDP sockets. Relevant information for the SLIP simulation is contained in the `simconfig` file. The `simconfig` file stores client port, server port, and IP address information.

<h2>Routing Protocol</h2>
This router implements the Distance Vector routing algorithm similarly to RIP. The Distance Vector routing algorithm will forward packets to the route with the smallest distance based on a metric. In this implementation, the metric is measured in hops. On startup the router will place entries into its routing table for networks that it is directly attached to. The routing table can then be updated with other routes when the router receives routing packets addressed to it. The routing packet has the following format:
```
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|                 Sender IP                     |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|             Number of routes (n)              |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|               destination 1                   |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|                 distance 1                    |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|               destination 2                   |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|                 distance 2                    |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|                   ...                         |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|               destination n                   |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|                 distance n                    |
+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
```

Routes are stored in the routing table and expire if they are not updated after 100 seconds. The initial routes that were added to the routing table on startup never expire.

<h2>IP Processing and Forwarding</h2>
This router uses IPv6. The router will read the IPv6 header to determine the destination address. If the destination address is the router's address, the router will process the packet as a routing packet. If the router has a route to the destination address, it will decrement the Hop Limit field in the header and place the packet in the outgoing queue and forward the packet on the interface determined by the routing algorithm. If no route exists for the destination address, the router will discard the packet and print an error message. The router uses a 64 bit network mask and will choose the route with the longest match in the event that there are multiple routes with the same metric.
