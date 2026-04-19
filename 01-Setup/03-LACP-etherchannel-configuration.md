# 03 LACP etherchannel configuration

## Objective
Configure Layer 3 EtherChannel links using LACP to provide redundancy between network devices.

## Overview
EtherChannel bundles multiple physical interfaces into a single logical link . In this design, Layer 3 EtherChannels are used between routers and switches to provide redundancy high availability.

## EtherChannel Summary

| Connection             |    Port-Channel    |     Subnet      |           IP Assignment          |
|------------------------|--------------------|-----------------|----------------------------------|
| Router1 ↔ Router2      | R1 Po 1 / R2 Po 2  |  10.20.10.0/30  | R1: 10.20.10.1 / R2: 10.20.10.2  |
| Router1 ↔ SW1          | R1 Po 2 / SW1 Po 1 |  10.20.20.0/30  | R1: 10.20.20.1 / SW1: 10.20.20.2 |
| Router2 ↔ SW2          | R2 Po 2 / SW2 Po 1 |  10.20.20.4/30  | R2: 10.20.20.5 / SW2: 10.20.20.6 |
| SW1 ↔ SW2              | SW1 Po 2 / SW2 Po2 |  10.30.30.0/30  | SW1: 10.20.30.1 / SW2: 10.20.30.2 |

## LACP Configuration (Router1 ↔ Router2)

### Router1

In Global Config mode:

```bash
interface range g1/1/3-4
no switchport
channel-group 1 mode active

interface port-channel1
ip address 10.20.10.1 255.255.255.252
```

### Router2

```bash
interface range g1/1/3-4
no switchport
channel-group 1 mode active

interface port-channel1
ip address 10.20.10.2 255.255.255.252
```

## Verification

### show etherchannel summary on Router1

<img width="750" height="386" alt="R1" src="https://github.com/user-attachments/assets/f0f2fb0f-c076-43af-a9f3-8d6661853840" />

### show etherchannel summary on Router2

<img width="726" height="369" alt="R2" src="https://github.com/user-attachments/assets/c56f4030-13ef-464d-b28c-803eec6a6c4d" />

### show etherchannel summary on SW1

<img width="754" height="385" alt="SW1" src="https://github.com/user-attachments/assets/b9272019-6230-4fbf-83ba-20c07f132892" />

### show etherchannel summary on SW2

<img width="771" height="367" alt="SW2" src="https://github.com/user-attachments/assets/ce8b89ba-b306-4dff-aebb-632d3cc3a4c9" />















