## CSET 2200 Lecture 12

---

## Review/Questions

---

## Layer 5 - Session Layer

- Handles persistent sessions between hosts
- Somewhat like TCP
- Often provides Authorization or Authentication
- Mostly unimplemented
- ZIP, X.225 examples

---

## Layer 6 - Presentation Layer

- Handles data conversions
- Also not often implemented
- Sometimes handles encryption
- Often blended with Application Layer

---

## Layer 7 - Application Layer

- The interesting one
- All of the protocols applications provide
- In OSI, mostly just concerned with display
- Lots of protocols here
- We'll cover a few useful ones today
    - BOOTP
    - DHCP
    - DNS

---

## BOOTP

- Provides IP assignment services to hosts
- Client broadcasts request
- Contains MAC
- Servers responds via broadcast with address
- Kinda like ARP in reverse
- UDP port 67 for server, 68 for replies

---

## DHCP

- Superseded Bootp
- Like BOOTP but supports pools
- Has many potential options
- Mask passed in options
- Gateway too along with DNS

---

## DHCP Process

- DHCP Discovery
    - Broadcast to 255.255.255.255
    - Sends MAC address
    - Sends IP address if previously assigned

---

## DHCP Process (contd)

- DHCP Offer
    - Server Sends offer
    - Contains IP address
    - Usually specifies options for lease length
    - Also options for gateway, mask, etc

---

## DHCP Process (contd)

- DHCP Request
    - Client sends request for offered IP
    - Can also ignore and not request
    - In case of multiple offers only one accepted

---

## DHCP Process (contd)

- DHCP Acknowledgement
    - Server sends ack or nak of offer
    - Client can short cut and just rerequest old address
    - Server will NAK if unavailable

---

## DHCP Options

- DHCP can send a bunch of other options
- Routers
- Boot Info
- DNS Servers
- Routes
- Config servers for VOIP

---

## DHCP Relay

- DHCP supports cross network pools
- Router on the edge forwards the broadcasts as unicast
- Handles replies

---

## DNS

- Domain Name System
- How friendly names get turned into IPs
- UDP/TCP port 53
- Complex protocol

---

## DNS (contd)

- DNS is a hierarchy
- Supports both forward and reverse lookups
    - Name to IP
    - IP to Name
- Reverse is a special zone in the root of the hierarcy

---

## DNS Root Servers

- Bootstraping problems
- How to find IP of Servers to use for lookups
- DNS hints file provides

---

## Delegation

- DNS servers rely on delegating parts of the tree
- Hints provide root, we then lookup each component
- com, net, org, us, etc top level domains
- Delegation to a TLD server for that TLD
- Continues down the tree until we find answer

---

## DNS SOA Record

- Start of Authority
- Includes "serial number"
- Timer for refresh, expiration
- Contact info for zone

---

## A Record

- "Standard" name lookup
- Returns IPV4 address of a name

---

## NS Record

- Used to delegate subzone to another DNS server

---

## MX Record

- Specifies "mail exchanger" for a domain
- Contains a priority number of the exchanger

---

## PTR Record

- Used for reverse DNS
- Usually in the in-addr.arpa zone

---

## Other record types

- TXT
- AAAA
- CNAME
- SRV

---

## Other DNS info

- TTL specifies how long we cache info
- Most servers support a AXFR type to transfer data
- Records can have multiple entries

---

## Wireshark examples

---

## Questions

---

## Next Lesson - starting some routing

- Chapter 20 - a basic understanding
- May cover some of 27
- https://en.wikipedia.org/wiki/History_of_the_Internet
