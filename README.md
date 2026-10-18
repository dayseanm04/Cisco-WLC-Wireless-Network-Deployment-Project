# Cisco WLC Wireless Network Deployment Project

## Overview

In this project I designed and built an enterprise network in Cisco Packet Tracer with a centralized Cisco 3504 Wireless LAN Controller (WLC) managing three access points. The wired side has department VLANs, redundant Layer 3 EtherChannel links, OSPF routing, DHCP, and a simulated internet connection.

The goal was to practice what a network admin does when rolling out wireless in a company: plan the VLANs and addressing, build the core network, then bring the WLC online and create separate corporate and guest WLANs.

<img width="1067" height="657" alt="network-diagram" src="https://github.com/user-attachments/assets/e10994ac-4277-4d01-af48-d2b60e91300e" />


> **Status: Paused.** I stopped this project partway through because Cisco Packet Tracer kept giving me problems with the wireless side of the lab. I moved my time to my [**Nagios Network Monitoring Project**](https://github.com/dayseanm04). Everything documented below was built and verified before I paused.

## Devices

- 2 × Cisco 3650 Layer 3 switches acting as edge routers (Router1, Router2)
- 2 × Cisco 3650 switches (SW1, SW2)
- 1 × Cisco 3504 Wireless LAN Controller (WLC1)
- 3 × wireless access points (WAP1–WAP3)
- Servers: DHCP, internal server
- Department PCs and a management PC
- Simulated internet: INET-R1, a switch, DNS server, web s

## VLANs

| VLAN | Name | Purpose | Network |
|------|------|---------|---------|
| 10 | HR | HR users | 192.168.0.0/24 |
| 20 | Administration | Admin users | 192.168.1.0/24 |
| 30 | IT | IT users (static IPs) | 192.168.2.0/24 |
| 50 | Management | WLC, APs, management PC | 192.168.50.0/24 |
| 200 | Servers | Internal servers | 10.0.0.0/24 |

## What I Built

### Network Design
- VLAN design separating departments, management, and servers
- IP addressing plan with loopbacks on every router and switch for device ID and management

### Core Network Setup
- Created VLANs and SVIs for inter-VLAN routing
- Built **Layer 3 EtherChannels with LACP** between routers and switches for redundancy
- Configured a trunk from SW1 to the WLC with a native VLAN











