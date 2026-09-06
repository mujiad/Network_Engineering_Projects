# Enterprise Client-Server Network Infrastructure with VLANs, DHCP, DNS, and NAT/PAT

## Project Overview

This project demonstrates the design and implementation of an enterprise-style network using Cisco Packet Tracer. The network supports multiple departments, centralized network services, inter-VLAN communication, secure device management, and connectivity to an external network.

The project was designed to simulate a small-to-medium business environment with separate networks for Administration, IT, Sales, Servers, and Network Management.

The network uses a Cisco Layer 3 switch for internal routing and an edge router for external connectivity and Network Address Translation (NAT/PAT).

---

## Project Objectives

The objectives of this project are to:

- Design and configure an enterprise-style network infrastructure.
- Implement VLAN segmentation for multiple departments.
- Configure trunk links between switches.
- Configure inter-VLAN routing using a Layer 3 switch.
- Configure centralized DHCP services.
- Implement DHCP relay using `ip helper-address`.
- Configure DNS services for hostname resolution.
- Configure HTTP and FTP services.
- Connect and configure network printers.
- Configure a Management VLAN for network device administration.
- Configure SSH for secure remote access.
- Configure an edge router for external network connectivity.
- Configure default routing between the internal network and edge router.
- Implement NAT/PAT to translate private IP addresses.
- Test and verify network connectivity and services.

---

# Network Topology

```text
                              EXTERNAL NETWORK
                                    
                              EXTERNAL-SERVER
                                     |
                                ISP-SWITCH
                                     |
                              203.0.113.0/24
                                     |
                                 R1-EDGE
                              NAT / PAT
                                     |
                                10.0.0.0/30
                                     |
                                  L3-SW1
                           Layer 3 Core Switch
                                     |
        -------------------------------------------------
        |                |              |               |
     SW-ADMIN          SW-IT         SW-SALES       SW-SERVER
        |                |              |               |
    ADMIN PCs          IT PCs       SALES PCs        Servers
    ADMIN Printer      IT Printer                    DHCP Server
                                                     DNS Server
                                                     Web Server
                                                     File Server
```

![Project2(https://github.com/mujiad/Enterprise Client-Server Network/Project2.png)
## Network Architecture

- The network follows a hierarchical design consisting of:

Core Layer
Access Layer
Server Network
Edge Network
External Network

## Core Layer
The Cisco 3560 Multilayer Switch acts as the core device and performs:

VLAN routing
Inter-VLAN routing
Default gateway services
DHCP relay
Routing to the edge router

## Access Layer
Cisco 2960 switches connect end-user devices including:

PCs
Printers
Servers

The access switches use VLANs and trunk links to communicate with the Layer 3 core switch.

## Edge Layer

The Cisco edge router provides:

Connectivity to the external network
Default routing
NAT
PAT
