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

