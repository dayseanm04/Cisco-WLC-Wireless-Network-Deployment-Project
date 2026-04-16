# 02 Configure Enterprise to Internet WAN Edge Connectivity

## Reference Topology

<img width="706" height="298" alt="Topology" src="https://github.com/user-attachments/assets/201e2c42-60e7-4c0f-ba59-5670aae5d0d8" />

## Objective
Configure point-to-point WAN links between the enterprise routers and INET-R1 for external network connectivity.

## Overview
This step establishes Layer 3 connectivity between the enterprise edge routers and the simulated internet using /30 subnets. These links represent public-facing WAN connections and allow communication with external services. 

## WAN Link Summary

| Connection        | Device A | Interface | IP Address   | Device B | Interface | IP Address   | Subnet Mask        |
|------------------|----------|-----------|--------------|----------|-----------|--------------|--------------------|
| Router1 ↔ INET-R1 | Router1 | G1/1/1    | 205.1.0.2    | INET-R1  | G1/0      | 205.1.0.1    | 255.255.255.252    |
| Router2 ↔ INET-R1 | Router2 | G1/1/1    | 205.2.0.2    | INET-R1  | G2/0      | 205.2.0.1    | 255.255.255.252    |

## INET-R1 configuration

In Global Config mode:

```bash
interface g1/0
ip address 205.1.0.1 255.255.255.252

```

## Router1 configuration

```bash
interface g1/1/1
ip address 205.1.0.2 255.255.255.252

```

## Verify

### show ip interface brief on INET-R1

<img width="821" height="120" alt="ISP-R1" src="https://github.com/user-attachments/assets/e6a4518b-f3ab-42e3-b0dc-42fd5a0ade63" />

### show ip int bri | include GigabitEthernet1/1/ on Router

<img width="773" height="116" alt="Router1" src="https://github.com/user-attachments/assets/be2fdbb6-5517-4219-9afe-5d7271913068" />
1


