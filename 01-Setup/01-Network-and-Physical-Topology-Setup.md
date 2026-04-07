# 01 Network and Physical Topology Setup

## Objective
Build the core network topology by connecting all devices and enabling Layer 3 routing on the switches to support the WLC and wireless access points.

## Devices Used
- Cisco 3650 (Router1)
- Cisco 3650 (SW1)
- Cisco 3650 (SW2)
- Cisco 3504 Wireless LAN Controller (WLC)
- 3 Wireless Access Points (WAP1, WAP2, WAP3)
- Management PC


## Network Information
- WLC IP Address: 192.168.50.254/24
- Management PC IP Address: 192.168.50.10/24 (Static)

## Physical Connections

### Router to Switch Connections
- Router1 G1/0/3 → SW1 G1/0/3
- Router1 G1/0/4 → SW1 G1/0/4
- Router1 G1/0/5 → SW2 G1/0/5
- Router1 G1/0/6 → SW2 G1/0/6

### Switch to Access Point Connections
- SW1 G1/0/11 → WAP1
- SW1 G1/0/12 → WAP2
- SW1 G1/0/13 → WAP3
