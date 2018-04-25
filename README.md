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

__Packet:__ Small bites of data chunks

__Packet switches:__ A method to move data through a network. Made of routers and linklayer switches.

When a packet arrive to a router:
* router looks up in a forward tabel, and then find which connection the packet should be sent at.


__Example:__ if a source system or a packet switch is sending a packet of L bits over a link with transmission rate R bits/sec, then the time to transmit the packet of L/R seconds
* L = number of bits
* R = transmissionspeed [bits/s]
* L/R = time in seconds
