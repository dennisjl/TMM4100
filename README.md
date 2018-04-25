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

Today, the most prevalent types of braodband residential access are __DSL__ (Digital subscriber line). One typically obtains DSL Internet access from the same local telephone company that provides wired local phone access. Phoneline carries both data and traditional phone signals simultaneously, which are encoded at different frequencies. This approach makes the DSL link appear as if there were 3 separate links, -----> phone and internet connection can shre DSL link

* Important characteristic of cable internet access is that its a shared broadcast medium. 
* Every packet sent by the head end travels downstream on every link to every home
* Every packet sent by a home travels upstream channel to head end
