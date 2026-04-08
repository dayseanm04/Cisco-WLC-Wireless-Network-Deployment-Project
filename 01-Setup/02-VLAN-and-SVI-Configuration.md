# 02 VLAN and SVI Configuration

## Objective
Configure initial VLANs, SVIs, and trunk links to enable network segmentation and inter-VLAN communication.

## VLAN Overview

| VLAN ID | Name         | Purpose                  | Subnet              | Gateway        |
|--------|-------------|--------------------------|---------------------|----------------|
| 50     | Management  | WLC and management traffic | 192.168.50.0/24     | 192.168.50.1   |
| 100    | corp | Initial WLAN VLAN   |          |        |
| 200    | Server-VLAN | Internal server network   | 10.0.0.0/24         | 10.0.0.1       |
