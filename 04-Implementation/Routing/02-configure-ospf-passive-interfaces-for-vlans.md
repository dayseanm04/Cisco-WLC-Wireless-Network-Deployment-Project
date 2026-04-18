# 02 Configure OSPF Passive Interfaces for VLANs

## Objective
Configure OSPF passive interfaces on VLAN interfaces to prevent unnecessary neighbor formation while still advertising network routes.

## Passive Interface Summary

| Device | Interface (VLAN) | VLAN ID | Network Purpose        | Passive |
|--------|------------------|--------|------------------------|---------|
| SW1    | VLAN 50          | 50     | Management Network     | Yes     |
| SW1    | VLAN 200         | 200    | Server Network         | Yes     |
| SW2    | VLAN 10          | 10     | HR Department          | Yes     |
| SW2    | VLAN 20          | 20     | Administration         | Yes     |
| SW2    | VLAN 30          | 30     | IT Department          | Yes     |

## SW1 config

In global config mode:

```bash
router ospf 1
passive-interface vlan 50
passive-interface vlan 200
```

## SW1 config

In global config mode:

```bash
router ospf 1
passive-interface vlan 10
passive-interface vlan 20
passive-interface vlan 30
```

## Verification

### show ip protocols on SW1

<img width="802" height="290" alt="SW1" src="https://github.com/user-attachments/assets/34c96118-a887-4d92-badc-1b6feb225424" />

### show ip protocols on SW2

<img width="871" height="314" alt="SW2" src="https://github.com/user-attachments/assets/e3f2578a-8110-43a1-8779-d0915edc7e2b" />

## Design Considerations
- Reduces unnecessary OSPF traffic on access networks.
