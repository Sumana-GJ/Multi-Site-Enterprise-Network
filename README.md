# Multi-Site Enterprise Network — Cisco Packet Tracer

## Project Overview
Designed and configured a simulated multi-site enterprise network using Cisco Packet Tracer. The lab demonstrates VLAN segmentation, inter-VLAN routing, dynamic routing, DHCP, NAT overload, access control, and secure remote device access.

## Technologies and Concepts
- Cisco Packet Tracer
- VLANs and 802.1Q trunking
- Router-on-a-stick inter-VLAN routing
- OSPF dynamic routing between R1 and R2
- DHCP address allocation
- NAT overload (PAT)
- Extended ACL-based access control
- SSH version 2 for secure remote access

## Network Features
- VLAN 10 — USERS
- VLAN 20 — ADMIN
- VLAN 30 — SUPPORT
- VLAN 40 — SERVERS
- Branch LAN — 192.168.50.0/24
- OSPF-enabled connection between R1 and R2

## Validation
Verified network operation using:
- `show vlan brief`
- `show interfaces trunk`
- `show ip interface brief`
- `show ip route ospf`
- `show ip nat translations`
- `show ip nat statistics`
- `show access-lists`
- `show ip ssh`
- Ping tests between HQ VLANs and the branch network
- SSH login from a PC to R1

## Project Files
- `Multi_Site_Enterprise_Network.pkt` — Packet Tracer topology and configuration
- `README.md` — Project documentation

## Notes
This is a learning and simulation project created in Cisco Packet Tracer. It is not a production network deployment.
