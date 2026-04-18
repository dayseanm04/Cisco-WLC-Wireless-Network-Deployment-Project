# 04 Configure Trunk and Native VLAN for WLC Integration

## Objective
Configure a trunk link between the SW1 and the Wireless LAN Controller (WLC1) and confige native VLAN for untagged traffic.

## Topology For Reference

<img width="384" height="274" alt="RT" src="https://github.com/user-attachments/assets/6463475c-392e-48c6-b807-ed2477066319" />


## Trunk Configuration Summary

| Interface | Mode  | Native VLAN | Allowed VLANs                | Description                  |
|----------|------|-------------|------------------------------|------------------------------|
| G1/1/1   | Trunk | 999         | 10, 20, 30, 50, 100, 200     | SW1 to WLC connection     |

### Config

On SW1 in global config mode:
```bash
interface g1/1/1
switchport mode trunk
switchport trunk native vlan 999
switchport trunk allowed vlan 10,20,30,50,100,200
```

## Verififcation

### show interface trunk on SW1

