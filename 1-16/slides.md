## CSET 2200

### Routing (RIP) and VLANs

---

## PC Example from last week

---

## Routing Information Protocol (RIP)

- Distance Vector routing protocol
- Occasionally broadcasts all routes
- Routers add one to each route before resending
- Hop count max of 15 (16 is infinity)

---

## Loop protection

- Split Horizon (Don't transmit out receive int)
- Poison Routes
- Hold Down timer

---

## Example

---

## RIP v1 vs v2

- v1 used all broadcasts
- Containe no mask information
- v2 uses multicast
- Also transmit subnet info

---

## RIP Implementation

---

## Other Routing information

---

## "Advanced" Layer 2

- VLANs
- Spanning Tree

---

## Virtual LANs

- Allow a switch to handle multiple broadcast domains
- 802.1q is the IEEE standard
- Uses the tag field of the Ethernet header

---

## VLAN (Contd)

- Used to seperate layer 3 networks
- Security and or Management reasons
- Need a router to route between them

---

## 802.1q

- Uses 0x8100 in the Ethertype field to identify tag
- Adds a 3 bit QoS field
- Adds a 1 bit Drop Eligibile bit
- 12 bit VLAN id

---

## VLAN id

- VLAN 0-4095
- 0 and 4095 reserved
- 1 is normally the default

---

## Trunk ports

- Allow a single cable or link to transit multiple VLANs
- Packets on the trunk are tagged
- One VLAN may be untagged

---

## Access ports

- Access ports transmit packets untagged
- Only contain a single VLAN

---

## Uses for VLANs

- Voice
- DMZ
- Guest Networks
- Segregtion of other traffic

---

## Configuring VLANs

- Done on the switch
- Cisco switch ports have multiple modes
    - trunk
    - access
    - dynamic

---

```
interface gi0/1
switchport mode trunk
```

---

```
interface gi0/2
switchport mode access
switchport access vlan 10
```

---

## Router interfaces

- Most router support trunk interfaces
- Can configure subinterfaces on different vlans
- Required to route between VLANs

---

## Example configuration

---

## Questions

---

## Next time - STP (Not stone temple pilots)

- Spanning tree

