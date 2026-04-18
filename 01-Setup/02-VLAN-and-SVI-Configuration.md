# 02 VLAN and SVI Configuration

## Objective
Configure initial VLANs, SVIs, and trunk links to enable network segmentation and inter-VLAN communication.

## VLAN Overview

| VLAN ID | Name       | Purpose                  | Subnet              | Gateway        |
|--------|-------------|--------------------------|---------------------|----------------|
| 30     | IT DPT      |  Information Technology  |  	192.168.0.0/24    |      .1        |
| 20     | Administration DPT   | Administration  |   192.168.1.0/24    |      .1        |
| 30     | IT DPT               | Information Technology  | 192.168.2.0/24  |     .1     |
| 50     | Management  | WLC and management traffic | 192.168.50.0/24   |      .1        |
| 100    | corp | Initial WLAN VLAN   |          |        |
| 200    | Server-VLAN | Internal server network   | 10.0.0.0/24         |     .1       |

### Example Configuration (VLAN)

In Global config mode on **SW1**:

```bash
vlan 50
name WAPs-VLAN
exit
```


## SVI Configuration

Layer 3 interfaces are configured on the switch to enable routing between VLANs.
| Interface     | IP Address      | Subnet Mask        | Description              |
|--------------|-----------------|--------------------|--------------------------|
| VLAN 50      | 192.168.50.1    | 255.255.255.0      | Management gateway       |
| VLAN 200     | 10.0.0.1        | 255.255.255.0      | Server VLAN gateway      |

### Example Configuration (SVI)

In Global config mode on **SW1**:

```bash
interface vlan 50
ip address 192.168.50.1 255.255.255.0
no shutdown
```

## Configure department VLANs on SW2

```bash
vlan <ID>
name <VLAN NAME>
interface range <START> <END>
switchport access vlan <ID>
```

### Configure SVI for the vlans

```bash
interface vlan <ID>
ip address <IP Address> <Subnet Mask>
no shutdown
```



