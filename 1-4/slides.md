---

## CSET 2200 Lecture 5

---

## Questions/Review

---

## Ethernet Devices

---

## Shared bus

---

## Repeater

- Layer 2 device
- Used to extend cable reach
- Limitations on max number

---

## Hub

- Layer 2 device
- Retransmits all receives frames on every port
- Basically a multiport repeater

---

## Hub (contd)

- No memory (forwards packets as received)
- Half Duplex
- Only single speed supported

---

## Hub (contd)

- Limit to number of segments and hubs (4 3 2)
- Electrical properties limit this
- Propogation takes time
- Need to be able to catch colissions

---

## Hub (contd)

- Mostly phased out these days for switches
- Sometimes used as active taps

---

## Bridge

- Bridges join two collision domains
- Have some intelligence to handle traffic flow
- Have memory, usually store and forward
- Allow networks to get grow
- Limit collisions

---

## Switch

- Switches address many issues hubs have
- Technically a type of bridge
- Limit traffic to necessary ports
- Each port has it's own collision domain

---

## Switch (contd)

- Required for full duplex communication
- In Full duplex mode essentially a PtP link
- Collissions impossible with only two stations

---

## Switch (contd)

- Also help with network size
- Since each segment is seperate, we don't have delay concerns
- Build an internal address table
- Learns by observing incoming traffic
- Once port of a MAC address known, does not flood packet

---

## Switch (contd)

- Loops still a problem
- Addressed in various ways we'll cover later

---

## Types of Switching

- Store and Forward
    - Receives entire packet before forwarding
    - Drops packets with errors
- Cut Through
    - Only looks at frame dest address then forwards
    - Propgates errors
- Fragment Free
    - Looks at first 64 bytes then cut through
- Adaptive
    - Switches between above modes based on types

---

## Questions

---

## Switching Gears

- Remaining Layer 2 topics
    - VLANs
    - Spanning Tree
    - Design
- Will revisit after some L3 as it makes sense

---

## Layer2 on to Layer3

---

## Diagram

---

## Basic Layer 3

- In TCP/IP this is IP
- Stands for Internet Protocol
- Usually IPv4 is what is referred to
- Addresses in dotted quad (129.2.3.4)

---

## Layer 3 networks

- Each network defined as a network and a mask
- Each Layer 3 network has a network address and a broadcast
- Similar in function to broadcast at layer 2
- Uses to decide if packet is local

---

## Mapping Layer 2 to Layer 3

- Need a way to map a given layer 3 address to a given layer 2 address
- Answer is ARP (Address Resolution Protocol)

---

## ARP

- Layer 2 protocol to aid layer 3
- Implemented on many technologies
- Replaced in IPv6 with Neighbor Discovery Protocol
- Defined in RFCs 826 and 903

---

## ARP (contd)

- Hosts use ARP to find a layer 2 address given a layer 3
- Request Packets are sent to the broadcast ethernet address
- Response packets are normally sent to the requestor

---

## ARP Packets

- Layer 2 EtherType of 0x0806 for Ethernet
- Length of Packet is determined by Layer 2 and layer 3 protocol
- For our purposes we care about Ethernet and IPv4

---

## ARP Packet Format 

| Length | Purpose |
|--------|---------|
| 2 | Hardware Type (1) |
| 2 | Protocol Type (0x0800)|
| 1 | Hardware Addr Length (6) |
| 1 | Protocol Addr Length (4) |
| 2 | Operation |
| 6 | Sender Hardware Address |
| 4 | Sender Protocol Address |
| 6 | Target Hardware Address |
| 4 | Target Protocol Address |

---

## Other ARP stuff

- Operation is 1 for request, 2 for reply
- Hosts normally cache arp
- Some hosts send intential arp broadcast
- Prepopulates caches

---

## Some examples

---

## Security concerns

---

## Questions

---

## Next Lesson

- Starting on real layer 3
- Now it gets more interesting
- https://en.wikipedia.org/wiki/IPv4
- Book 20, 21
- We'll be here for a bit

---

