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

| Connection             |    Port-Channel    |     Subnet      |           IP Assignment          |
|------------------------|--------------------|-----------------|----------------------------------|
| Router1 ↔ Router2      | R1 Po 1 / R2 Po 2  |  10.20.10.0/30  | R1: 10.20.10.1 / R2: 10.20.10.2  |
| Router1 ↔ SW1          | R1 Po 2 / SW1 Po 1 |  10.20.20.0/30  | R1: 10.20.20.1 / SW1: 10.20.20.2 |
| Router2 ↔ SW2          | R2 Po 2 / SW2 Po 1 |  10.20.20.4/30  | R2: 10.20.20.5 / SW2: 10.20.20.6 |
| SW1 ↔ SW2              | SW1 Po 2 / SW2 Po2 |  10.30.30.0/30  | SW1: 10.20.30.1 / SW2: 10.20.30.2 |










