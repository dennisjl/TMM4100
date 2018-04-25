# TMM4100
KTN-Notes

# Chapter 1: Computer networks and the Internet

### Internet:
Network that interconnects hundreds of millions of computing devices throughout the world.
All devices are called hosts or end systems.

### End systems (Hosts):
Connected together by a network of communication links and __packets switchets__
A packet switch takes a packet arriving on one of it's incoming communication links and forwards that packet on one of it's outgoing communication links.
Two most prominent types:
1. Router
2. Link-layer switches

### Network protocols:
A protocol defines the format and the order of messages exchanges between two or more communication entities

Also the actions taken on transmission and/or receipt of a message or other event.

### TCP/IP:
Two of the most important protocols in the internet. IP specifies the format of the packets that are sent and receives among routers and end systems.

Internet applications run on end systems - they dont run in the packet switches in the network core. Packet switches does not concern with the application that is the source or sink of data.


### API:
__Application Programming Interface (API)__, specifies how a program running on an end system ask the Internet infrastructure to deliver data to a specific destination running on another end system. 

End systems attached to Internet provides an API




## The Network Edge (1.2):
__Host= End-systems__. Can be further divided into two categories:
1. Client
2. Server

Applications and end systems = _edge of the network_

__Access network:__ the network that physically connects an end system to the first router. Does this on a path from end system to other distant end system.

__DSL:__ (Digistal Subscriber Line): The most prevalent type of broadband residentaial access.
* Typically obatined from local phone company that provides wired local phone access.
* Phoneline carries both data and traditional phone signal at different frequencies.
** Makes DSL link appear as if there were 3 separate links, ----> phone and internet connection can share DSL link

Important characteristic of cable internet access:
* It is a shared broadcast medium
* Every packet sent by the head end travels downstream on every link to every home
* Every packet sent by a home travels upstream channel to head end

__LAN:__ (Local Area Network): used to connect an end system to the edge router. Many types of LAN technology.
* Ethernet is by far the most prevalent access technology.
Ethernet users use twisted-pair copper wire to connect to an Ethernet switch, which is connected into the large internet.





## The Network Core (1.3):
In a network application, End system exchange messages with each other. Messages can contain anything the app designer wants.

#### How to send message from source end system to destination system:
The source breaks long messages into smaller chunks of data, aka __packets__. Inbetween source and destination, each packet travels through communication links and packet. Packets are transmitted over each communication link at a rate equal to full transmission rate of the link.

#### Packet: 
Small bites of data chunks 
* Usually have multiple links attached to it.
* For each link, the packet switch has an outputbuffer, which property is to store packets that the router is about to send into that link. Plays a keyrole in packet switching.

Two fundamental approaches to moving data through network:
__Packet switches:__ A method to move data through a network. Made of routers and linklayer switches.
__Circuit switching:__ A method where the resources needed along a path to provide communivation session between the end systems.

When a packet arrive to a router:
* router looks up in a forward tabel, and then find which connection the packet should be sent at.

__Forwarding table:__ maps destination addresses to the routers outbound links.


__Example:__ if a source system or a packet switch is sending a packet of L bits over a link with transmission rate R bits/sec, then the time to transmit the packet of L/R seconds
* L = number of bits
* R = transmissionspeed [bits/s]
* L/R = time in seconds

#### Store-and-forward transmission:
The method most packet switches use at the inputs to the links.

Properties:
* The packet switch must receive the entire packet before it can begin to transmit the first bit of the packet onto the outbound link
* Total transmission delay: N * L/R, where N = total connections given N-1 routers.
* Extra delay can occure due to waiting for the previous package (__que delay__)



## Delay, Loss and Throughput in Packet-Switched Networks (1.4):

__Processing delay:__ time required to check the header of a package and find out where it is supposed to go

__Queuing delay__: time required waiting for the other packages to get sent on the link

__Transmission delay:__ time required to push packets on the link. Defined by L/R. ((number of bits)/(transmission speed))

__Propagation delay:__ time required to travel from one node to the next. d/s

__Total Nodal delay:__ sum of those 4 above.

__Total end-to-end delay:__ time required for the packet to travel from start to end, throught the routers. If there are several swithces, we use the transmission delay as well (dtrans)
* dend-to-end = N(dprocess + dtrans + dprop)
* N-1 routers in this example. assumes that the network are uncongested, s.a. que delay disappear.


## Protocol Layers and their Service Models (1.5):
### Protocol Layering:
To provide structure to the design of network protocols, the network desginers organize protocols, and the network hardware and software that implements the protocols in layers. excist 5 of them:
1. Application layer
2. Transport layer
3. Network layer
4. Link layer
5. Physical layer

### 1. Application Layer:
Where the network applications and application reside. Includes many protocols s.a:
* HTTP
* SMTP
* FTP

Distributed over multiple end systems, with the application in one end-system using the protocol to exchange packets of info with the application in another end system.
* Refer to this packet of info at the application layer as a message

### 2. Transport Layer:
Provides end-end-communication.

2 main transport protocols:
1. TCP
2. UDP

TCP provides connection-oriented services to its applications. Includes guaranteed delivery of application-layer message to the destiantion and flowcontrol

UDP provides connectionless service to its applications. No-frill service that provide no reliability, no flow control, and no congestion control.


### 3. Network layer:
Responsible for moving network-layer packets (datagrams) from one host to another. 

The internet transport-layer protocol in a source host passes a transport-layer protocol in a source host passes a transport-layer segment and a destination address to the network layer.

Includes the celebrated IP protocol, which defines the fields in the datagram as well as how the end systems and routers act on these fields.


### 4. Link layer:
Routes a datagram through a series of routers between the source and destination. 

__how to move a packet from one node to the next (in a route):__ the network layer relies on the services of the link layer. Services provided by the link layer depend on the specific link-layer protocols that is employed over the link. 

Refer to the link-layer packets as frames.

Job: move entire frames from one network element to an adjacent network element.


### 5. Physical layer:
The job of the physical layer is to move individual bits within the frame from one node to the next.

the protocols in this layer are again link dependent and further depend on the actual transmission medium of the link
