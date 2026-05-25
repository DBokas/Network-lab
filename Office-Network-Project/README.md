# Office Network Project

## Overview
This project shows a small office network using Cisco Packet Tracer. The network was designed to demonstrate networking concepts including VLAN segmentation, Inter VLAN routing, DHCP, DNS, and structured IP addressing.

The network consists of four separate departments connected through access switches to a central core switch and router. Centralised DHCP and DNS services are used to manage addressing and internal name resolution across the network.

---

# Network Topology

## Network Structure
The office network contains:

- 4 Department VLANs
- 4 Access Switches
- 1 Core Switch
- 1 Router
- 1 DHCP Server
- 1 DNS Server
- Planned future services:
  - File Server
  - Web Server
  - Email Server

Each department operates within its own VLAN and subnet to simulate office-style network segmentation.

---

# Technologies & Concepts Used

## Networking Technologies
- VLAN segmentation
- Inter-VLAN routing
- Router-on-a-Stick configuration
- DHCP
- DNS
- DHCP Relay (`ip helper-address`)
- Switching & Routing fundamentals
- Wireless networking fundamentals
- Structured IP addressing

## Software
- Cisco Packet Tracer

---

# Inter-VLAN Routing

Inter-VLAN routing was implemented using router subinterfaces configured with IEEE 802.1Q encapsulation.

Each VLAN was assigned:
- A dedicated subinterface
- A default gateway
- Independent IP address

DHCP relay (ip helper-address) was configured to allow devices in different VLANs to receive IP addresses from the DHCP server.

---

# DHCP Configuration

The DHCP server was configured with:
- Separate DHCP pools for each VLAN
- Unique default gateways
- DNS server assignment
- Automatic IP address allocation

This allows all departmental devices to dynamically receive valid network configurations.

---

# DNS Configuration

The DNS server was configured with internal DNS records for:
- DHCP Server
- DNS Server
- Planned internal services
- Intranet alias (CNAME)

This demonstrates basic internal enterprise name resolution.

---

# Testing & Validation

The following tests were successfully completed:

- Devices successfully received DHCP addresses
- Devices within separate VLANs successfully communicated
- Inter-VLAN routing verified through ping testing
- DNS records successfully resolved internally
- Router subinterfaces confirmed operational

Testing was performed using:
- ICMP Ping
- Packet Tracer Simple PDU testing
- DHCP address verification

---

# Troubleshooting

Several networking issues were encountered during development and configuration.

## Issues Encountered
- Initial VLAN communication failures
- Incorrect VLAN assignments on switch ports
- DHCP requests not crossing VLAN boundaries
- Routing configuration inconsistencies

## Resolution
These issues were resolved by:
- Verifying VLAN membership
- Confirming trunk connections
- Configuring router subinterfaces correctly
- Implementing DHCP relay using `ip helper-address`
- Testing connectivity between all network segments

---

# Planned Future Improvements

Planned future additions to the project include:
- File server implementation
- Internal web server hosting
- Email server configuration
- Access Control Lists (ACLs)
- Enhanced network security
- Network redundancy
- Monitoring and logging systems

---

# Screenshots

## Included Documentation
- Full network topology
- VLAN configurations
- Router interface configuration
- DHCP configuration
- DNS configuration
- Inter-VLAN ping tests
- Device IP assignments

---

# Skills Demonstrated

This project demonstrates practical understanding of:
- Enterprise-style network segmentation
- Layer 2 switching
- Layer 3 routing
- DHCP and DNS services
- Network troubleshooting
- Structured network design
- Documentation and validation practices
