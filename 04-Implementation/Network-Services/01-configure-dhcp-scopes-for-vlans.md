 01 Configure DHCP Scopes for VLANs

## Objective
Configure DHCP scopes to dynamically assign IP addresses to devices across multiple VLANs, including wireless infrastructure.

## DHCP Scope Summary

| Scope Name            | VLAN | Subnet              | Default Gateway   | Start IP        | Max Users | Notes                          |
|----------------------|------|---------------------|-------------------|-----------------|-----------|--------------------------------|
| HR-DPT               | 10   | 192.168.0.0/24     | 192.168.0.1      | 192.168.0.5    | 20        | HR department users          |
| Administration-DPT   | 20   | 192.168.1.0/24     | 192.168.1.1      | 192.168.1.5    | 20        | Administrative users           |
| WAP Pool             | 50   | 192.168.50.0/24     | 192.168.50.1      | 192.168.50.10   | 5         | Includes WLC address           |


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

<img width="968" height="173" alt="DHCP-POOL" src="https://github.com/user-attachments/assets/2b5f726b-6787-4d86-8adb-b23c5568ca7b" />

## Configuration Notes
- Each VLAN has its own DHCP scope to maintain proper segmentation.
- Default gateway addresses correspond to the SVI configured on the switch.
- The WAP pool includes the WLC IP to allow access points to discover the controller.
- IT devices will use static IP addressing.




