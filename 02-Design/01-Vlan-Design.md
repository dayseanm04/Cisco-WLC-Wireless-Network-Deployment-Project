# VLAN Design

## Overview
This document shows how VLANs are used in the network to separate traffic.
The design includes management, corporate, and server VLANs to support the WLC, access points, and internal resources. 

## VLAN Summary

The following VLANs are used to segment wired users by department. This improves security, organization, and traffic control across the network.

| VLAN ID | Name                | Department             | Purpose                          | Subnet | Default Gateway |
|--------|----------------------|------------------------|----------------------------------|--------|-----------------|
| 10     | HR DPT               | Human Resources        | HR user devices and resources    | 192.168.0.0/24  | .1     |
| 20     | Administration DPT   | Administration         | Administrative staff devices     | N/A    | N/A             |
| 30     | IT DPT               | Information Technology | IT staff and management systems  | N/A    | N/A             |

| VLAN ID | Name         | Purpose                          | Subnet              | Default Gateway   |
|--------|-------------|----------------------------------|---------------------|-------------------|
| 50     | Management  | WLC and network management       | 192.168.50.0/24     | 192.168.50.1      |
| 100    | Corp        | Corporate wireless clients       | N/A                 | N/A               |
| 200    | Server-VLAN | Internal servers and services    | 10.0.0.0/24         | 10.0.0.1          |

## VLAN Design Details

### VLAN 50 – Management
- Used for WLC andWAP management
- Includes management PC and WAPs
- Provides centralized control of wireless infrastructure

### VLAN 200 – Server VLAN
- Dedicated network for internal servers
- Isolated from user VLANs for security
- Provides backend services (DHCP etc.)
