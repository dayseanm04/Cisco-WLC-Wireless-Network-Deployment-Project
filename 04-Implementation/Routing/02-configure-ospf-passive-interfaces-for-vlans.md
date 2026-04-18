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
