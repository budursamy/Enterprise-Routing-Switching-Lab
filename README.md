# Enterprise Routing & Switching Lab | Cisco Packet Tracer

A two-site enterprise network built in Cisco Packet Tracer. Each site has its own VLANs, a multilayer core switch, and access switches. The two sites are connected over a WAN link and exchange routes with OSPF.

![Full topology](screenshots/full-topology.png)

## Topology Overview

- **2 sites** connected by a serial WAN link (`30.0.0.0/30`), each with a router and a multilayer core switch.
- **Site A:** VLANs 10, 20, 30 using subnets `192.168.10.0`, `192.168.20.0`, `192.168.30.0`.
- **Site B:** VLANs 40, 50, 60 using subnets `172.16.40.0`, `172.16.50.0`, `172.16.60.0`.
- **Per site:** router, multilayer core switch, and three access switches with end devices color-coded by VLAN.

## What Was Configured

| Area | Details |
|------|---------|
| **VLANs & Trunking** | VLAN segmentation per site, 802.1Q trunks between core and access switches |
| **VTP** | Core switch as VTP Server, access switches as VTP Clients |
| **EtherChannel** | Link aggregation between core and access switches |
| **Inter-VLAN Routing** | SVIs on the multilayer core switch |
| **STP / RSTP** | Loop prevention across the switching layer |
| **OSPF** | Dynamic routing between routers and across the WAN link between the two sites |
| **DHCP** | Automatic IP assignment for each VLAN |

## Verification

- **OSPF:** neighbor and route verification from the CLI: `screenshots/ospf-cli-verification.png`
- **Connectivity:** successful ICMP (ping) tests between hosts in different VLANs and across sites: `screenshots/ping-test.png`

![OSPF CLI verification](screenshots/ospf-cli-verification.png)
![Ping test](screenshots/ping-test.png)

## Project Files

- `Enterprise-switching&routing-lab.pkt`: the full Packet Tracer project (open with Cisco Packet Tracer)
- `screenshots/`: topology, OSPF verification, and ping test

## Tools

Cisco Packet Tracer, Cisco IOS CLI

## Author

**Budur Samy Mohamed**: Information Systems Graduate (Networks Specialization) | CCNA Trained

