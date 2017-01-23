## CSET 2200

### Lecture 3 - OSI Model/TCP Model/Network Theory

---

## Review network history

![Cisco AGS](AGS.jpg)

---

## The OSI model

#### AKA that thing you need to learn but don't directly use

---

## The OSI Model

![OSI Model](OSI.jpg)

<div class="notes">

* Joint ISO and CCITT
* 1984 published
* Abstract model of networking
* Influenced later designs
* Still used for reference
* Things at each layer speak to each other via PDU (Protocol Data Units) using above and below layers
</div>
---

## Ways to remember it

Programmer's don't need to see pretty applications

---

## Ways to remember it

Please do not throw sausage pizza away

![Mmmm Pizza](Pizza.jpg)

---

## Ways to remember it

People don't need those stupid packets anyways

![Token Ring](TR.jpg)

---

## Ways to remember it

Please do not teach students pointless acronyms

---

## Physical Layer

* Data Unit: Bit
* Electrical
* Various technologies (Ethernet/Token Ring/Wifi)

<div class="notes">
* Defined largely by IEEE (Institute of Electical and Electronics Engineers)
* Working groups define electrical signals
* May be light in the case of fiber
* May also be radio waves
* Bluetooth, Zigbee, Wifi, Token Ring, Ethernet all examples
</div>

---

## Data Link Layer

* Data Unit: Frame
* Reliable Transport
* Ethernet - 802.2

<div class="notes">

* Connections between local nodes in LAN
* Adjacent nodes in WAN (PtP)
* Provides syncronization
* Adds error control

</div>
---

## Network Layer
* Data Unit: Packet
* Not guaranteed to be reliable
* May split packets if too big
* IP

<div class="notes">

* Connectionless model
* Provides host addressing (MAC vs IP)
* Provides forwarding of data between layer 2 networks (Router)
* IP/IPv6/ICMP/IPX

</div>
---

## Transport Layer
* Data Unit: Datagram, Segment
* Provides multiplexing and flow control
* UDP, TCP

<div class="notes">

* Adds connection oriented services to Network
* Not ALL are connection oriented (UDP)
* Mutiplexing
* Reliability
* TCP, UDP

</div>
---

## Session Layer
* Handles Burrito Delivery (Just seeing if you're paying attention)
* Handles sessions and establishment of connections
* Nothing really in TCP/IP model

<div class="notes">

* Can handle connection restoriation
* AAA sometimes handled here
* X25 and Appletalk ZIP examples

</div>
---

## Presentation Layer
* Handles converting data between formats
* Allows program to be absolved of conversions
* Presentation layer is usually OS, but may be application

<div class="notes">

* Might convert file formats (ASCII/EBDIC)
* Serialization of program data can happen here (Raw data to JSON or XML)
* Application level encryption like SSL is here too

</div>
---

## Application Layer

* Application all the things
* Handles higher level protocals implemented in the application
* Examples include SMTP, NNTP, FTP

<div class="notes">

* Much higher level protocols that deliver data, etc
* DNS, DHCP, BootP will be discussed in class
</div>
---

## TCP/IP Model

![OSI vs TCP](TCPModel.gif)

<div class="notes">
* Implemented in practice
* Based on OSI model, but collapses some for simplicity
* Application, Presentation and Session just moved to application
* Most of these done in software anyways
</div>
---

## Comparisons of Models

* TCP/IP simplified
* I believe 5 layers
* Segregates protocols more logically

<div class="notes">
* Example of theoritical model vs implementation
* Much less loosely defined than OSI model
</div>

---

## Questions?

---

## General Network Discussion

---

## Next week 

