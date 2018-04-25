# TMM4100
KTN-Notes

## Chapter 1: Computer networks and the Internet

##### Internet:
Network that interconnects hundreds of millions of computing devices throughout the world.
All devices are called hosts or end systems.

##### End systems:
Connected together by a network of communication links and __packets switchets__
A packet switch takes a packet arriving on one of it's incoming communication links and forwards that packet on one of it's outgoing communication links.
Two most prominent types:
1. Router
2. Link-layer switches

##### TCP/IP:
Two of the most important protocols in the internet. IP specifies the format of the packets that are sent and receives among routers and end systems.


Internet applications run on end systems - they dont run in the packet switches in the network core. Packet switches does not concern with the application that is the source or sink of data.

End systems attached to the Internet provide an __Application Programming Interface (API)__ that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination running on another end system.
