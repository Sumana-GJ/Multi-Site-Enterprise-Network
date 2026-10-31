
# Multi-Site Enterprise Network — Cisco Packet Tracer

## Project Overview

Designed and configured a simulated multi-site enterprise network using Cisco Packet Tracer. The lab demonstrates VLAN segmentation, inter-VLAN routing, dynamic routing, DHCP, NAT overload, access control, and secure remote device access.

## Network Topology
![Network Topology](Packet_Tracer_Screenshots/01-Network-Topology.png)

The simulated network consists of:

- **Headquarters (HQ):** Four VLANs supporting USERS, ADMIN, SUPPORT, and SERVERS.
- **WAN connection:** R1 and R2 connected through a point-to-point network using OSPF.
- **Branch network:** A separate LAN connected to R2.

## IP Addressing and VLANs
![VLAN Configuration](Packet_Tracer_Screenshots/02-Vlan-Brief.png)

| VLAN |    Name    |     Network     |  Default Gateway |
|------|------------|-----------------|------------------|
|  10  | USERS      | 192.168.10.0/24 |   192.168.10.1   |
|  20  | ADMIN      | 192.168.20.0/24 |   192.168.20.1   |
|  30  | SUPPORT    | 192.168.30.0/24 |   192.168.30.1   |
|  40  | SERVERS    | 192.168.40.0/24 |   192.168.40.1   |
|------| Branch LAN | 192.168.50.0/24 |   192.168.50.1   |

The HQ VLANs use router-on-a-stick inter-VLAN routing through R1.

## Technologies and Concepts
![Trunk Port Configuration](Packet_Tracer_Screenshots/03-Trunk-Ports.png)

![OSPF Neighbor Verification](Packet_Tracer_Screenshots/04-OSPF-Neighbor.png)

- Cisco Packet Tracer
- VLANs and 802.1Q trunking
- Router-on-a-stick inter-VLAN routing
- OSPF dynamic routing between R1 and R2
- DHCP address allocation
- NAT overload (PAT)
- Extended ACL-based access control
- SSH version 2 for secure remote access

## Network Features
![OSPF Branch Route](Packet_Tracer_Screenshots/05-OSPF-Branch-Route.png)

- Segmented HQ network using four VLANs.
- DHCP configured for automatic client addressing.
- OSPF configured between R1 and R2 to exchange routes.
- NAT overload configured on R1.
- Extended ACL `BLOCK_ADMIN_BRANCH` restricts ADMIN VLAN access to the branch network.
- SSH v2 configured for secure remote management of R1.

## Validation
![Connectivity Tests](Packet_Tracer_Screenshots/06-Connectivity-Tests.png)

![ACL Configuration](Packet_Tracer_Screenshots/07-ACL-Configuration.png)

![ACL Blocked Ping](Packet_Tracer_Screenshots/08-ACL-Blocked-Ping.png)

![NAT Translations](Packet_Tracer_Screenshots/09-Nat-Translations.png)

Network operation was verified using Cisco IOS commands and connectivity tests:

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
  
![SSH Version 2 Verification](Packet_Tracer_Screenshots/10-SSH-Verification.png)

## Project Files

- `Multi_Site_Enterprise_Network.pkt` — Packet Tracer topology and configuration
- `README.md` — Project documentation

## Notes

This is a learning and simulation project created in Cisco Packet Tracer. It is not a production network deployment.

- `README.md` — Project documentation
