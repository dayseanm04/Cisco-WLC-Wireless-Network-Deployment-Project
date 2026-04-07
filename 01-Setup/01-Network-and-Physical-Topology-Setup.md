# 01 Network and Physical Topology Setup

## Objective
Build the core network topology by connecting all devices and enabling Layer 3 routing on the switches to support the WLC and wireless access points.

## Devices Used
- Cisco 3650 (Router1)
- Cisco 3650 (SW1)
- Cisco 3650 (SW2)
- Cisco 3504 Wireless LAN Controller (WLC)
- 3 Wireless Access Points (WAP1, WAP2, WAP3)
- Management PC


## Network Information
- WLC IP Address: 192.168.50.254/24
- Management PC IP Address: 192.168.50.10/24 (Static)

## Physical Connections

### Router to Switch Connections
- Router1 G1/0/3 → SW1 G1/0/3
- Router1 G1/0/4 → SW1 G1/0/4
- Router1 G1/0/5 → SW2 G1/0/5
- Router1 G1/0/6 → SW2 G1/0/6

Note: if you forget what which port is connected to which port use **cdp** to dicover the ports and where where connected to.

<img width="809" height="188" alt="R1" src="https://github.com/user-attachments/assets/9dfee66f-0bfa-4782-9cdf-46b0e63b8dcd" />

<img width="767" height="141" alt="SW1" src="https://github.com/user-attachments/assets/4bd23c55-ab11-4c38-bb26-d683ec5bcbc8" />

<img width="777" height="137" alt="SW2" src="https://github.com/user-attachments/assets/b85fe1b6-5db0-43da-b95b-82acab8ddccd" />

### Switch to Access Point Connections
- SW1 G1/0/11 → WAP1
- SW1 G1/0/12 → WAP2
- SW1 G1/0/13 → WAP3

### Management Connection
- SW1 G1/0/14 → Management PC

### Switch to PC Connections

#### HR Department (HR DPT)
- HR-PC1 → SW2 G1/0/1
- HR-PC2 → SW2 G1/0/2
- HR-PC3 → SW2 G1/0/3
- HR-PC4 → SW2 G1/0/4

#### Administration Department (Administration DPT)
- A-PC1 → SW2 G1/0/10
- A-PC2 → SW2 G1/0/11
- A-PC3 → SW2 G1/0/12
- A-PC4 → SW2 G1/0/13

#### IT Department (Information Technology DPT)
- IT-PC1 → SW1 G1/0/20
- IT-PC2 → SW1 G1/0/21

## Initial Switch Configuration

### Enable Layer 3 Routing on Core Switches

On **SW1** and **SW2**:

```bash
enable
configure terminal
ip routing
end
write memory
```

## Reference Topology

<img width="839" height="511" alt="intial-topology" src="https://github.com/user-attachments/assets/d7d4dfce-c101-4027-9ae3-d53a9c3fc108" />



