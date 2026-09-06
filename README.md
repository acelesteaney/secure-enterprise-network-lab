# ACANEY - Secure Enterprise Network Infrastructure

## Project Overview

This project presents the design, implementation and security of the network infrastructure of **ACANEY**, a fictional enterprise environment developed as a practical networking and cybersecurity project.

The infrastructure was designed to provide network segmentation, controlled communication between departments, centralized network services and secure administration of Cisco network devices.

The entire infrastructure was implemented and tested using **Cisco Packet Tracer**.

---

## Company Context

**ACANEY** is a fictional company composed of several departments requiring isolated and controlled network environments.

The network infrastructure was designed around the following departments:

- Direction
- Comptabilité
- Ressources Humaines
- IT
- Serveurs

The objective is to provide each department with its own network while allowing only the necessary communications between them.

---

## Project Objectives

The main objectives of this project were to:

- Design an enterprise network architecture
- Segment the network using VLANs
- Implement VLSM addressing
- Configure inter-VLAN routing
- Deploy DHCP, DNS and HTTP services
- Control inter-VLAN communications using ACLs
- Secure network administration using SSH
- Implement switch port security
- Test and validate the network infrastructure

---

## Network Architecture

The infrastructure uses a **Router-on-a-Stick** architecture.

The router and switch are connected through an **802.1Q trunk**, allowing multiple VLANs to be transported over a single physical link.

### VLAN Architecture

| VLAN | Department | Network |
|------|------------|---------|
| 10 | Direction | 192.168.10.8/29 |
| 20 | Comptabilité | 192.168.10.0/29 |
| 30 | RH | 192.168.10.16/29 |
| 40 | IT | 192.168.10.24/29 |
| 50 | Servers | 192.168.10.32/29 |
| 225 | Native VLAN | Management / Native |

---

## Routing

Inter-VLAN communication is provided by the router using **Router-on-a-Stick**.

Each VLAN is associated with a dedicated router sub-interface serving as its default gateway.

---

## Network Services

The infrastructure includes:

- DHCP
- DNS
- HTTP
- Inter-VLAN routing

DHCP is used for end-user devices, while servers in the server VLAN use static addressing.

---

## Network Security

Several security mechanisms were implemented.

### Access Control Lists

Extended ACLs were configured to control traffic between VLANs according to the organization's communication requirements.

The security policy allows necessary services such as:

- DNS
- HTTP
- SSH for IT administration
- ICMP for authorized management traffic

Unnecessary inter-department communication is restricted.

### Secure Administration

Cisco devices were secured using:

- Local user authentication
- Privileged EXEC authentication
- SSH version 2
- RSA cryptographic keys
- VTY line restrictions

### Switch Port Security

Port Security was implemented on user access ports using:

- Sticky MAC addresses
- Maximum MAC address limitation
- Shutdown violation mode

---

## Testing and Validation

The infrastructure was tested to verify:

- VLAN connectivity
- DHCP address allocation
- DNS resolution
- HTTP accessibility
- Inter-VLAN communication
- ACL enforcement
- SSH access
- Port Security operation

Both authorized and restricted communications were tested.

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- IPv4
- VLSM
- VLAN
- 802.1Q
- Router-on-a-Stick
- DHCP
- DNS
- HTTP
- ACL
- SSH
- RSA
- Port Security

---

## Skills Developed

This project provided practical experience in:

- Enterprise network design
- IP addressing and subnetting
- VLAN segmentation
- Routing and switching
- Network services
- Network access control
- Cisco device administration
- Network security fundamentals
- Troubleshooting and network validation

---

## Future Improvements

This project is intended to evolve into a more complete enterprise infrastructure.

Future versions may include:

- Windows Server and Active Directory Domain Services
- Linux servers
- Centralized authentication
- Firewall implementation
- IDS/IPS
- Network monitoring
- SIEM integration
- Security event analysis
- Incident detection and response

---

## Project

**ACANEY - Enterprise Network Infrastructure**

Developed as a practical networking and cybersecurity project using Cisco Packet Tracer.
