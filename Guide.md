# NetPractice guide

## TCP: Transmission Control Protocol

A communication protocol that allows for the transmission of data between devices. It is connection-oriented, meaning that a connection is established between the devices before data is transmitted. It is reliable, as it ensures that data is delivered in the correct order and without errors. It is also stream-oriented, meaning that data is transmitted as a continuous stream of bytes.

---
## IP Address: Internet Protocol Address

A unique numerical label assigned to each device connected to a network that uses the Internet Protocol for communication. It serves as an identifier for the device on the network and allows for the routing of data packets to the correct destination.

---
## Public vs. Private IP Addresses

Public IP addresses are globally unique and can be accessed from the internet. Private IP addresses are used within a local network and are not accessible from the internet. Network Address Translation (NAT) is used to translate private IP addresses to public IP addresses when communicating with devices outside the local network.

---
## Subnet Mask

A 32-bit number that is used to divide an IP address into network and host portions. It is used to determine which part of an IP address is the network address and which part is the host address. Subnet masks are typically written in dotted decimal notation, such as 255.255.255.128

---
## CIDR Notation: Classless Inter-Domain Routing Notation

I'll help you fill out the CIDR notation table, starting with /30 and including the commonly used notations. I'll present it in markdown format.

---

| CIDR Notation | Subnet Mask     | IP Range                | Total IPs  |
| ------------- | --------------- | ----------------------- | ---------- |
| /30           | 255.255.255.252 | x.x.x.0 - x.x.x.3       | 4          |
| /29           | 255.255.255.248 | x.x.x.0 - x.x.x.7       | 8          |
| /28           | 255.255.255.240 | x.x.x.0 - x.x.x.15      | 16         |
| /27           | 255.255.255.224 | x.x.x.0 - x.x.x.31      | 32         |
| /26           | 255.255.255.192 | x.x.x.0 - x.x.x.63      | 64         |
| /25           | 255.255.255.128 | x.x.x.0 - x.x.x.127     | 128        |
| /24           | 255.255.255.0   | x.x.x.0 - x.x.x.255     | 256        |
| /23           | 255.255.254.0   | x.x.x.0 - x.x.x+1.255   | 512        |
| /22           | 255.255.252.0   | x.x.x.0 - x.x.x+3.255   | 1,024      |
| /21           | 255.255.248.0   | x.x.x.0 - x.x.x+7.255   | 2,048      |
| /20           | 255.255.240.0   | x.x.x.0 - x.x.x+15.255  | 4,096      |
| /19           | 255.255.224.0   | x.x.x.0 - x.x.x+31.255  | 8,192      |
| /18           | 255.255.192.0   | x.x.x.0 - x.x.x+63.255  | 16,384     |
| /17           | 255.255.128.0   | x.x.x.0 - x.x.x+127.255 | 32,768     |
| /16           | 255.255.0.0     | x.x.0.0 - x.x.255.255   | 65,536     |
| /8            | 255.0.0.0       | x.0.0.0 - x.255.255.255 | 16,777,216 |

---
## Switch

A network device that connects multiple devices within a local area network (LAN). It operates at the data link layer of the OSI model and uses MAC addresses to forward data to the correct destination. Switches are more efficient than hubs, as they only forward data to the intended recipient rather than broadcasting it to all devices on the network.

---
## Router

A network device that connects multiple networks together and forwards data packets between them. Routers operate at the network layer of the OSI model and use IP addresses to determine the best path for data to reach its destination. Routers are essential for connecting devices on different networks, such as a local network to the internet.

---
### Routing Table

A table maintained by a router that contains information about the available routes to different networks. It includes the network address, subnet mask, gateway, and interface for each route. The router uses this information to determine the best path for forwarding data packets to their destination.

In netpractice it only constains 2 elements:

destination: the network address of the destination network
Next hop: the IP address of the next hop router or the outgoing interface

---

# Level hints:

---
## Level 1 (Connect 2 ip's in the same subnet mask range)

### Solution:
  - Set both devices ip's in the same subnet mask range [copy&paste ip's and change last digit
---
## Level 2 (Connect 2 ip's in the same subnet mask range)

### Solution:
- Set both devices ip's to the subnet mask range [copy&paste ip's and change last digit]
- Set both devices subnet mask to be the same [copy&paste subnet mask]
---
## Level 3 (Connect 3 ip's in the same subnet mask range)

### Solution:
- Set all devices ip's to the subnet mask range [copy&paste ip's and change last digit]
- Set the subnet mask to be the same for all devices [copy&paste subnet mask]
---
## Level 4 (Connect 2 ip's via a router)

### Solution:
- Set all devices ip's to the subnet mask range [copy&paste ip's and change last digit]
- Set the subnet mask to be the same for all devices [copy&paste subnet mask]
---
## Level 5 (Connect 2 ip's with different subnet mask ranges via a router)

### Solution:
- Connect R1 to A1
- Connect R2 to A2
- Route from Ax to Rx default=>ip of Rx
---
## Level 6 (Connect host to internet)

### Solution:
- Connect R1 to A1
- Set router to default gateway
- Route internet to A1/28
---
## Level 7 (Connect host1 to host2 via 2 routers)

### Solution:
- clear all
- Set all masks to /28
- fill all
---
## Level 8 (Connect 2 host to internet and each other)

### Solution:
- Default routes
- set all masks the same
- set internet connection
- fill interfaces in ranges
- set r1 connections from (same as internet) to R21

---
## Level 9 (Connect a bunch of hosts and 2 to the internet)

### Solution:
- clear all
- set defaults
- create 111.111.111.left and route to internet /25
- fill bottom and route to r1
- create 222.222.222.right and route to both
- create 42.42.42.middle

---
## Level 10

### Solution:
- clear all
- set masks and fill basic
- connect interface to r11
- default r1
- 193
- 194

---
