## CSET 2200

### Network Address Translation

---

## Review

---

## Questions

---

## The problem(s)

- IP addresses are scarce
- Renumbering networks is hard
- Private networks need to connect

---

## Network Address Translation

- Converts one set of IP's to another
- Supports several different methodologies
    - One to One
    - Port Mapping
    - Masquerade (PAT)

---

## One to One NAT

- Maps one external IP to one internal
- Used to remap networks
- Also sometime used to translate private to connect

---

## One to Many (Port mapping)

- Maps one external IP and Port to an inside IP and Port
- Often used to expose external services
- Very common - SOHO routers call port mapping

---

## Masquerade (PAT)

- Allows many interal IPs to show as one external IP
- Preserves IP space
- Very common at both residential and commercial
- Uses port rewriting to allow multiple connections

---

## Other NAT Types

- NAT types can be combined
- Expose port on external IP that is mapped to
- PAT can be with a pool

---

## Examples and Application

---

## Cisco implementation

- Outside and inside interface
- Local and global IPs

---

## Example of Local/Global

---

## Cisco Implentation (Contd)

- Tag inside and outside interfaces
- Create access list to match traffic (optional)
- Create NAT rules

---

## Example

```
interface GigabitEthernet0/0
 ip address 72.240.28.131 255.255.255.0
 ip nat outside
interface GigabitEthernet0/1
 ip address 192.168.1.1 255.255.255.0
 ip nat inside
access-list 101 permit ip 192.168.1.0 0.0.0.255 any
ip nat inside source list 101 interface GigabitEthernet0/0 overload
```

---

## Example 2

```
interface FastEthernet0/0
 ip address 72.240.58.190 255.255.255.252 secondary
 ip address 72.240.53.106 255.255.255.248
 ip access-group 121 in
 ip nat outside
interface FastEthernet0/1
 ip address 192.168.1.1 255.255.255.0
 ip nat inside
access-list 100 permit ip 192.168.1.0 0.0.0.255 any
access-list 121 permit ip 12.37.9.0 0.0.0.255 host 72.240.53.107
access-list 121 permit ip 72.241.56.64 0.0.0.7 host 72.240.53.107
access-list 121 deny   ip any host 72.240.53.107
access-list 121 permit ip any host 72.240.53.106
access-list 121 permit ip 72.240.0.0 0.0.1.255 host 72.240.53.108
access-list 121 permit ip 64.254.140.0 0.0.0.31 host 72.240.53.108
access-list 121 permit ip 64.254.34.0 0.0.0.31 host 72.240.53.108
access-list 121 permit ip 64.254.134.0 0.0.0.31 host 72.240.53.108
access-list 121 permit ip 64.254.134.0 0.0.0.255 host 72.240.53.108
access-list 121 permit ip 72.240.0.0 0.1.255.255 host 72.240.53.108
ip nat inside source list 100 interface FastEthernet0/0 overload
ip nat inside source static tcp 192.168.1.8 135 72.240.53.107 135 extendable
ip nat inside source static tcp 192.168.1.8 137 72.240.53.107 137 extendable
ip nat inside source static tcp 192.168.1.8 138 72.240.53.107 138 extendable
ip nat inside source static tcp 192.168.1.8 139 72.240.53.107 139 extendable
ip nat inside source static tcp 192.168.1.8 445 72.240.53.107 445 extendable
ip nat inside source static tcp 192.168.1.8 1680 72.240.53.107 1680 extendable
ip nat inside source static tcp 192.168.1.20 443 72.240.53.108 8443 extendable
```

---

## Demonstration

---

## Questions

---

## Monday - Firewalls
