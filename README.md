# Layered-Network-Security-with-ASAs

This project simulates a layered enterprise-grade network security infrastructure using Cisco ASA Firewalls, Core/Distro Switches, VLANs, and Server Segmentation — all designed and built in Cisco Packet Tracer.

Project Overview

The topology mimics a secure corporate network (e.g., bank or enterprise) featuring:

-Three-layer firewall defense (Perimeter → DMZ → Honeypot)
-Internet connectivity via Router
-VLAN segmentation for different departments (Admin, HR, IT, Guest)
- Honeypot deception zone for attackers
- Dynamic IP assignment via DHCP
- Access Control Lists (ACLs) for traffic filtering
- Static routing & NAT on ASA


Firewall Roles

ASA1 - Perimeter Firewall - Connects to Internet Router, blocks unwanted traffic, allows core LAN 
ASA2 - DMZ Firewall - Protects production server; only Admin/IT VLANs allowed 
ASA3 - Honeypot Firewall - Redirects Guest VLAN to honeypot server, logs all other traffic

Technologies Used

- Cisco Packet Tracer
- Cisco ASA 5506-X
- Cisco 2911 Router
- Cisco 2960 and 3650 Switches
- DHCP, NAT, ACL, VLAN, Static Routing
- Client Laptops & Servers

Configuration Highlights

Multilayer Core Switch
- VLANs: Admin (10), HR (20), IT (30), Guest (99)
- SVI IPs and routing enabled
- IP helper for DHCP

Distribution Switches (x4)
- Access ports assigned per VLAN
- Trunk links to Core

DHCP Server
- DHCP pools for all VLANs
- Connected directly to Core switch

ASA Firewalls
- NAT & ACLs per role
- Interface security levels
- Inter-ASA communication and segmentation
- Honeypot server isolation

Screenshot
![image](https://github.com/user-attachments/assets/cd8cb488-21b4-4f75-9436-c78ba06ef5a4)



Files Included

- `.pkt` Cisco Packet Tracer topology file
- `README.md` (this file)
- CLI configuration documentation (multilayer switch, ASA1-3, Router, DHCP, switches)

Simulation Goals

- Simulate external attacker traffic hitting the perimeter (ASA1)
- Route malicious users from Guest VLAN through honeypot (ASA3)
- Log unauthorized access
- Ensure legit departments only reach production servers
- Practice advanced configuration & network design


Author

Nabin Shrestha  


