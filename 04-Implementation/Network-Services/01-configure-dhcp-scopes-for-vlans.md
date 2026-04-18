 01 Configure DHCP Scopes for VLANs

## Objective
Configure DHCP scopes to dynamically assign IP addresses to devices across multiple VLANs, including wireless infrastructure.

## DHCP Scope Summary

| Scope Name            | VLAN | Subnet              | Default Gateway   | Start IP        | Max Users | Notes                          |
|----------------------|------|---------------------|-------------------|-----------------|-----------|--------------------------------|
| WAP Pool             | 50   | 192.168.50.0/24     | 192.168.50.1      | 192.168.50.10   | 5         | Includes WLC address           |
| HR-DPT               | 10   | 192.168.10.0/24     | 192.168.10.1      | 192.168.10.5    | 20        | HR department users          |
| Administration-DPT   | 20   | 192.168.20.0/24     | 192.168.20.1      | 192.168.20.5    | 20        | Administrative users           |

## Static Addressing

| Department | VLAN | Addressing Type | Notes                          |
|-----------|------|-----------------|--------------------------------|
| IT DPT    | 30   | Static          | Used for IT management systems |

## Example Configuration (WAP Pool)
- Pool Name: WAP Pool
- Default Gateway: 192.168.50.1
- Start IP Address: 192.168.50.10
- Subnet Mask: 255.255.255.0
- Maximum Number of Users: 5
- WLC Address: 192.168.50.254

## Configuration Notes
- Each VLAN has its own DHCP scope to maintain proper segmentation.
- Default gateway addresses correspond to the SVI configured on the switch.
- The WAP pool includes the WLC IP to allow access points to discover the controller.
- IT devices will use static IP addressing.




