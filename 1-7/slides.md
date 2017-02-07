## CSET2200 Lecture 8

---

## Review/Questions

---

## Quick review of packet moving

---

## CIDR

- CLassless Inter-domain Routing

---

## The problem

- Classful networks wasteful
- Aggregation was poor
- Route bloat
- Limited big networks

---

## Example - UT

---

## How to solve it

- Allow segmenting network on any bit
- Allow grouping of networks (aggregation)
- Allocation of smaller networks

---

## VLSM

- Variable length subnet mask
- Allows networks to be sized differently
- Core concept of CIDR

---

## Available Networks

---

## Aggregation

- Adjacent networks can be combined where distinction not needed
- Allows more efficient routing
- Large blocks allocated to providers which split them

---

## Example - UT Again

---

## Matching Networks

- Done with Bitwise AND
- Network to match AND subnet - network to match
- Remember 1 is our care bit

---

## Examples

- 64.254.140.4/27
- 64.254.140.165/28
- 72.240.0.0/15
- 131.183.222.23/23

---

## Questions

---

## Next session - more VLSM practice
