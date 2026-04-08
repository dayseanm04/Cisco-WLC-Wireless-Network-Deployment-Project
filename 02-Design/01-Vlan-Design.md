# VLAN Design

## Overview
This document shows how VLANs are used in the network to separate traffic.
The design includes management, corporate, and server VLANs to support the WLC, access points, and internal resources. 

## VLAN Summary

| VLAN ID | Name         | Purpose                          | Subnet              | Default Gateway   |
|--------|-------------|----------------------------------|---------------------|-------------------|
| 50     | Management  | WLC and network management       | 192.168.50.0/24     | 192.168.50.1      |
| 100    | Corp        | Corporate wireless clients       | N/A                 | N/A               |




