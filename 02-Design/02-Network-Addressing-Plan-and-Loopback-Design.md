# 02 Network Addressing Plan and Loopback Design

## Overview
This document defines the IP addressing scheme used in this project including VLANs, loopback interfaces, and port-channel links used for connectivity between network devices.

## VLAN Addressing Plan

| VLAN ID | Name                 | Department / Role        | Subnet              | Default Gateway   |
|--------|----------------------|--------------------------|---------------------|-------------------|
| 10     | HR DPT               | Human Resources          | 192.168.10.0/24     |       |
| 20     | Administration DPT   | Administration           | 192.168.20.0/24     |     |
| 30     | IT DPT               | Information Technology   | 192.168.30.0/24     |     |
| 50     | WAPs / Management    | WLC and Access Points    | 192.168.50.0/24     |       |
| 200    | Server VLAN          | Internal Servers         | 10.0.0.0/24         |         |

## Addressing Notes
- VLAN 50 is used for wireless infrastructure, including the WLC and access points.
- VLAN 200 is reserved for servers.


## Loopback Interfaces
Loopback interfaces will be used used for Network device identification, testing, and management.

| Device   | Loopback Interface | IP Address     | Subnet Mask | Purpose                        |
|----------|--------------------|----------------|-------------|--------------------------------|
| Router1  | Loopback0          | 10.10.0.10     | /32         | Router identification/MGNT     |
| Router2  | Loopback0          | 10.10.0.20     | /32         | Router identification/MGNT     |
| SW1       | Loopback0          | 10.10.0.1     | /32         | SW1 identification/MGNT        |
| SW2       | Loopback0          | 10.10.0.2     | /32         | SW2 identification/MGNT        |


## Port-Channel Addressing

Port-channels are used to provide aggregated and redundant Layer 3 links between network devices.

| Connection             | Port-Channel | Subnet         | IP Assignment      |
|------------------------|-------------|-----------------|--------------------|
| Router1 ↔ Router2      |             |                 |                    |










