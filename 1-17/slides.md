## CSET 2200

### Spanning tree

---

## Questions

---

## Completion of VLAN Demo

---

## Spanning Tree - The problem

- Loops
- Need to add redundent links
- Backup without intervention

---

## Solution - Spanning Tree

- Develops a loop free topology
- Defined in 802.1D
- Updated over the years
- 802.1Q is most recent

---

## Spanning Tree (contd)

- Spanning tree selects a root bridge
- Bridge with lowest priority
- If tied lowest mac

---

## Spanning tree (contd)

- Each switch finds lowest cost path to root
- Costs vary based on technology
- Ethernet uses bandwidth
- Lowest cost port is root port (RP)

---

## Spanning tree (contd)

- Each segment finds lowest cost to root
- Port connecting that segment is designated port (DP)
- All ports that aren't RP or DP block

---

## BPDU

- Spanning tree communicates with BPDU
- Stands for Bridge Protocol Data Units
- Exchanged regurally (2 seconds)

---

## Learning process

- Ports comes up and blocks
- Listening (Waiting for BPDU)
- Learning (Populates MAC table but still block)
- Forwarding (Passes data)
- Could also be Blocking or Disabled

---

## Time to converge

- Default for Listen and Learn each 15 seconds
- Means ports take 30 seconds to come active
- Can cause outages as networks reconfigure

---

## VLANs and STP

- All VLANs shared a tree origionally
- Two technologies to solve
    - Multiple Spanning Tree (MST)
    - Per VLAN spanning tree (PVST)

---

## Other improvements

- Rapid Spanning Tree improves convergence time
- RPVST

---

## Design Considerations

- Want root towards the middle of the network
- Careful root design is important in large network
- With PVST want all links active between VLANs

---

## Example

---

## Questions

---

## Next session TBD - will email

- Maybe NAT
- Maybe ACL
- Need to review Lab

