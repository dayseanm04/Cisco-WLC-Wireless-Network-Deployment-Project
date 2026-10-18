# Cisco WLC Wireless Network Deployment Project

## Overview

In this project I designed and built an enterprise network in Cisco Packet Tracer with a centralized Cisco 3504 Wireless LAN Controller (WLC) managing three access points. The wired side has department VLANs, redundant Layer 3 EtherChannel links, OSPF routing, DHCP, and a simulated internet connection.

The goal was to practice what a network admin does when rolling out wireless in a company: plan the VLANs and addressing, build the core network, then bring the WLC online and create separate corporate and guest WLANs.

<img width="839" height="511" alt="topology-1" src="https://github.com/user-attachments/assets/0888205d-ca56-41e6-b8d6-df642b84c799" />

> **Status: Paused.** I stopped this project partway through because Cisco Packet Tracer kept giving me problems with the wireless side of the lab. I moved my time to my [**Nagios Network Monitoring Project**](https://github.com/dayseanm04). Everything documented below was built and verified before I paused.

## Devices

- 2 × Cisco 3650 Layer 3 switches acting as edge routers (Router1, Router2)
- 2 × Cisco 3650 switches (SW1, SW2)
- 1 × Cisco 3504 Wireless LAN Controller (WLC1)
- 3 × wireless access points (WAP1–WAP3)
- Servers: DHCP, NTP, internal server
- Department PCs and a management PC

