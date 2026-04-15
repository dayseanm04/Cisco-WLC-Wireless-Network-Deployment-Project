# 01 Network and Physical Topology Setup

## Objective
Build the core network topology by connecting all devices and enabling Layer 3 routing on the switches to support the WLC and wireless access points.

## Devices Used
- Cisco 3650 (Router1 and Router2)
- Cisco 3650 (SW1 and SW2)
- Cisco 3504 Wireless LAN Controller (WLC)
- 3 Wireless Access Points (WAP1, WAP2, WAP3)
- Management PC


## Network Information
- WLC IP Address: 192.168.50.254/24
- Management PC IP Address: 192.168.50.10/24 (Static)

## Physical Connections

### Switch to Access Point Connections
- SW1 G1/0/11 → WAP1
- SW1 G1/0/12 → WAP2
- SW1 G1/0/13 → WAP3
- SW1 G1/1/1 → WLC1 G1

### Management Connection
- SW1 G1/0/14 → Management PC

### Router to Router Connections
- Router1 G1/1/3 → Router2 G1/1/3
- Router1 G1/1/4 → Router2 G1/1/4

### Router to Switch Connections
- Router1 G1/0/3 → SW1 G1/0/3
- Router1 G1/0/4 → SW1 G1/0/4
- Router2 G1/0/5 → SW2 G1/0/5
- Router2 G1/0/6 → SW2 G1/0/6

### Switch to Switch Connections
- SW1 G1/0/2 → SW2 G1/0/2
- SW1 G1/0/3 → SW2 G1/0/3

Note: if you forget what which port is connected to which port use **cdp** to dicover the ports and where where connected to.


<img width="791" height="177" alt="R1" src="https://github.com/user-attachments/assets/79e47510-0ae3-4a2a-950b-b498fff1a5ea" />


<img width="820" height="169" alt="R2" src="https://github.com/user-attachments/assets/9bb03f7b-ec91-4404-aa73-d2649ff371ee" />

<img width="792" height="156" alt="SW1" src="https://github.com/user-attachments/assets/4435b8a7-2bf1-4c06-a295-bcc8ad44d62d" />


<img width="785" height="154" alt="SW2" src="https://github.com/user-attachments/assets/db95b333-bbb4-484e-bc93-573978ae3717" />


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





