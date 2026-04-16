# 01 External Network and Internet Simulation Setup

## Reference Topology

<img width="697" height="342" alt="INET" src="https://github.com/user-attachments/assets/2130dc3d-305c-47e2-9111-3c2ea6d2bd74" />

## Objective
Simulate an external (internet) network and configure connectivity between the internal enterprise network and external services such as DNS and web servers.


## Overview
I will use this external network  to represent the internet. This includes an Internet router, a switch, and public-facing services such as DNS and web servers. 

## Topology Overview

### Enterprise to Internet Connections

| Device        | Interface | Connected To | Interface |
|--------------|----------|--------------|----------|
| Router1      | G1/1/1   | INET-R1      | G1/0     |
| Router2      | G1/1/1   | INET-R1      | G2/0     |

### Internet Internal Connections

| Device        | Interface | Connected To     | Interface |
|--------------|----------|------------------|----------|
| INET-R1      | G0/0     | INET-SW1         | G0/1     |
| INET-SW1     | G1/1     | INET-DNS-SRV     | NIC      |
| INET-SW1     | G2/1     | INET-WEB-SRV     | NIC      |
| INET-SW1     | G3/1     | INET-MGNT-PC1    | NIC      |

## IP Addressing (External Network)

| Device           | Interface | IP Address     | Subnet Mask        | Description         |
|------------------|----------|----------------|--------------------|---------------------|
| INET-R1          | G0/0     | 172.16.1.1     | 255.255.255.0      | Gateway for INET LAN |
| INET-DNS-SRV     | NIC      | 172.16.1.10    | 255.255.255.0      | DNS Server          |
| INET-WEB-SRV     | NIC      | 172.16.1.20    | 255.255.255.0      | Web Server          |
| INET-MGNT-PC1    | NIC      | 172.16.1.30    | 255.255.255.0      | Management PC   |

## Configure default gateway for INET Services

On INET-R1 in Global Config Mode:

```bash
interface g0/0
ip address 172.16.1.1 255.255.255.0
```

























