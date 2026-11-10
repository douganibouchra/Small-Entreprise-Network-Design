# Enterprise Network Design & Implementation

## Project Overview
This project consists of designing and implementing a small enterprise network using Cisco Packet Tracer. The network connects three departments (HR, Finance, and IT) through VLAN segmentation, inter-VLAN routing, and centralized network services.

## Network Topology
- 1 Cisco Router
- 1 Managed Switch
- Multiple PCs across three departments
- 1 Server
- 1 Network Printer

## Network Segmentation

| Department | VLAN | Network | Gateway |
|---|---|---|---|
| HR | 10 | 192.168.10.0/24 | 192.168.10.1 |
| Finance | 20 | 192.168.20.0/24 | 192.168.20.1 |
| IT | 30 | 192.168.30.0/24 | 192.168.30.1 |

## Technologies & Configurations

- **VLANs:** Logical network segmentation for the three departments.
- **802.1Q Trunking:** Carries traffic from multiple VLANs between the switch and router.
- **Router-on-a-Stick:** Enables inter-VLAN communication using router subinterfaces.
- **DHCP:** Automatically assigns IP addresses to network devices.
- **DNS:** Resolves the internal domain `www.company.local`.
- **HTTP:** Hosts an internal company web page.
- **Access Control Lists (ACLs):** Restricts communication between HR and Finance while allowing IT to communicate with all departments.

## Server Configuration
- Server IP: `192.168.30.10`
- DHCP service for all three VLANs.
- DNS service with the record `www.company.local`.
- HTTP service hosting an internal webpage.

## Security Implementation
Two extended ACLs were configured:
- ACL 110: Blocks HR from accessing Finance.
- ACL 120: Blocks Finance from accessing HR.
- Other permitted traffic remains accessible, including communication with the IT department.

## Testing & Verification
The following tests were performed:
- DHCP address assignment.
- Inter-VLAN connectivity.
- DNS name resolution.
- Internal website accessibility.
- ACL security and traffic restrictions.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI
- Networking protocols and services

## Project Objective
To gain practical experience in enterprise network design, configuration, segmentation, network services, and basic network security.