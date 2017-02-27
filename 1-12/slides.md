## CSET 2200 Lecture 13

---

## Review/Questions

---

## Homework Question 3

---

## DNS Review

- DNS is Hierachal
- Maps name to IP and IP to Name
- A records = hosts
- NS records delegate
- PTR records map IP to host

---

## Tying it all together

- So far covered LAN
- Some WAN
- How do we tie them together

---

## Internetworks

- Connecting individual networks
- Internet is the prime example
- Architecture has varied over the years

---

## History of internetworks

- Ethernet long king for LAN
- How LAN connects has varied over years

---

## Early days

- Slow links
- Expensive dedicate circuits
- Little redundancy

---

## Getting more complex

- Links get faster
- Still largely dedicated
- Some virtual connections over dedicated

---

## Modern days

- VPN slowly replacing dedicated circuits
- Ethernet taking over WAN/MAN circuits
- Common for many companies to only have internet

---

## Connecting Internetworks

- We've discussed Layer 2 connections
- Routers connect layer 2 segments
    - This should be review

---

## What is a router

- Essential specialized PC
- Has multiple network cards
- Makes decisions based on layer 3 data
- These days may be a switch too

---

## How routers work

- Read packet
- Examine Layer header
- Examine Route table for destination network
- Resolve layer 2 address of next hop
- Forward Packet

---

## Routing tables

- Route tables also called Routing Information Base
- Store Information needed to move packets
    - Destination Network
    - Destination Mask
    - Next Hop
    - Optional metric

---

## How packets are routed

- Most specific match wins
- If tie, pick the lowest of highest metric

---

## Default Route

- Route of 0.0.0.0/0
- Where packets get sent if no other match present
- Most hosts have ONLY default route

---

## Questions

---

## To summarize

- Networks link computers together
- Started as low speed links
- Over time got faster

---

## OSI Model

- Physical
- Data Link
- Network
- Transport
- Session
- Presentation
- Application

---

## TCP/IP Model

- Physical (Optional)
- Link
- Internet
- Transport
- Application

---

## Next Session

- Summary (contd)

