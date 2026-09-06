### Cisco Small Office Network — Configuration Documentation
## 1. Project Overview

- This project demonstrates the configuration of a small office network using Cisco Packet Tracer. The network consists of two departments:

Administration
Technical Support

- The network uses VLAN segmentation, IPv4 addressing, VLAN trunking, and Router-on-a-Stick inter-VLAN routing.

### Network Devices

| Device           | Quantity | Purpose                          |
|------------------|----------|----------------------------------|
| Cisco 1941 Router | 1        | Inter-VLAN routing               |
| Cisco 2960 Switch | 1        | LAN switching and VLAN segmentation |
| PCs               | 4        | End-user devices                 |

2. Network Topology
Physical connections

![Project1](https://github.com/mujiad/Network_Engineering_Projects/blob/main/Small%20Office%20Network%20Configuration%20%E2%80%94%20Cisco%20Packet%20Tracer/Project1.png)

## Cable connections

- Use Copper Straight-Through cables:

        R1 GigabitEthernet0/0 → SW1 GigabitEthernet0/1
        ADMIN-PC1 → SW1 FastEthernet0/1
        ADMIN-PC2 → SW1 FastEthernet0/2
        TECH-PC1 → SW1 FastEthernet0/3
        TECH-PC2 → SW1 FastEthernet0/4

## 3. IP Addressing Plan
| Device     | VLAN | IP Address    | Subnet Mask     | Default Gateway |
|------------|------|---------------|-----------------|-----------------|
| R1 VLAN 10 | 10   | 192.168.10.1  | 255.255.255.0   | —               |
| R1 VLAN 20 | 20   | 192.168.20.1  | 255.255.255.0   | —               |
| ADMIN-PC1  | 10   | 192.168.10.10 | 255.255.255.0   | 192.168.10.1    |
| ADMIN-PC2  | 10   | 192.168.10.11 | 255.255.255.0   | 192.168.10.1    |
| TECH-PC1   | 20   | 192.168.20.10 | 255.255.255.0   | 192.168.20.1    |
| TECH-PC2   | 20   | 192.168.20.11 | 255.255.255.0   | 192.168.20.1    |

