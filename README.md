# Materialyze's Virtual Enterprise Network Simulation Lab

This project simulates a small enterprise network environment utilizing EVE-NG. This lab includes VLAN segmentation, inter-VLAN routing, static and dynamic routing, NAT, DHCP, and access control lists (ACLs). It is designed to demonstrate core networking concepts aligned with CompTIA Network+ and Cisco CCNA certification objectives.

---

## Project Goals

- [X] ~~Create a scalable network topology simulating a real-world enterprise environment~~ Completed 14 July 2025
- [ ] Configure VLANs and inter-VLAN routing to segment departments
- [ ] Implement DHCP and NAT for IP management and internet access
- [ ] Apply ACLs to control network traffic
- [ ] Practice troubleshooting in a controlled lab environment
- [ ] Simulate outside breaches and how to quickly isolate affected systems, identify breaches, and minimize damage

---

## Technology and Tools

- [EVE-NG ](https://www.eve-ng.net/)
- IPv4 & IPv6 Subnetting
- OSPF (Open Shortest Path First)
- Static Routing
- NAT, DHCP, ACLs
- Wireshark
- Git / Github for version control

---

## Network Topology

![Network Diagram](network-topology)

**Node Overview:** 

- 3 VLANs: VPC
- 2 Routers: Mikrotik 6.49.19
- 2 Switches: Cisco vIOS m.03.201.7
- 1 Firewall: FortiGate 7.6.3
