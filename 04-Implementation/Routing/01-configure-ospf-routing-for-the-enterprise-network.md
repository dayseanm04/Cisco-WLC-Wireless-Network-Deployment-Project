# 01-Configure-OSPF-Routing-for-the-Enterprise-Network

## Objective
Configure OSPF across routers and Layer 3 switches to enable full network communication.

# Topology For Reference

<img width="893" height="455" alt="TFR" src="https://github.com/user-attachments/assets/029af53b-30b1-4816-ba93-afe7752be321" />

## OSPF Network Advertisement Summary

| Device   | Network Advertised     | Wildcard Mask   | Area | Description                          |
|----------|------------------------|------------------|------|--------------------------------------|
| Router1  | 10.10.0.10            | 0.0.0.0          | 0    | Loopback interface                   |
| Router2  | 10.20.0.0             | 0.0.255.255      | 0    | Core links (Port-Channels)           |
| SW1      | 10.10.0.1             | 0.0.0.0          | 0    | Loopback interface                   |
| SW1      | 10.20.0.0             | 0.0.255.255      | 0    | Core links                           |
| SW1      | 192.168.50.0          | 0.0.0.255        | 0    | WAP-MGNT VLAN                      |
| SW1      | 10.0.0.0              | 0.0.0.255        | 0    | Server VLAN                          |
| SW2      | 10.10.0.2             | 0.0.0.0          | 0    | Loopback interface                   |
| SW2      | 10.20.0.0             | 0.0.255.255      | 0    | Core links                           |
| SW2      | 10.0.0.0              | 0.0.0.255        | 0    | Server VLAN                          |
| SW2      | 192.168.0.0           | 0.0.0.255        | 0    | HR VLAN                              |
| SW2      | 192.168.1.0           | 0.0.0.255        | 0    | Administration VLAN                  |

## Example Configuration (Router1)

```bash
router ospf 1
network 10.10.0.10 0.0.0.0 area 0
network 10.20.0.0 0.0.255.255 area 0
```

## Configuration Notes
- OSPF process ID 1 is used across all devices.
- Loopback interfaces are advertised using a /32 wildcard (0.0.0.0).
- Core infrastructure links are summarized using a broader wildcard mask.
- VLAN networks are advertised to allow inter-VLAN routing.

