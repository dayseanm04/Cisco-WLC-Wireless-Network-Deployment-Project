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
- Router2 G1/0/5 → SW2 G1/0/5
- Router2 G1/0/6 → SW2 G1/0/6

### Switch to Switch Connections
- SW1 G1/0/2 → SW2 G1/0/2
- SW1 G1/0/3 → SW2 G1/0/3


Note: if you forget what which port is connected to which port use **cdp** to dicover the ports and where where connected to.

<img width="771" height="135" alt="R1" src="https://github.com/user-attachments/assets/89c1c3cc-8489-400e-af92-012dc5e0b7ba" />

<img width="796" height="132" alt="R2" src="https://github.com/user-attachments/assets/f5f9ed50-7203-4721-aa5f-eed5f07ce543" />

<img width="792" height="156" alt="SW1" src="https://github.com/user-attachments/assets/4435b8a7-2bf1-4c06-a295-bcc8ad44d62d" />


<img width="785" height="154" alt="SW2" src="https://github.com/user-attachments/assets/db95b333-bbb4-484e-bc93-573978ae3717" />



### Switch to Access Point Connections
- SW1 G1/0/11 → WAP1
- SW1 G1/0/12 → WAP2
- SW1 G1/0/13 → WAP3
- SW1 G1/1/1 → WLC1 G

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

<img width="797" height="455" alt="topology-1" src="https://github.com/user-attachments/assets/c3c06300-fe9a-49e8-acb1-8a054ef49a8e" />





