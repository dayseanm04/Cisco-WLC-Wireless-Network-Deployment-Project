# 04 External Network and Internet Simulation Setup

## Reference Topology

<img width="697" height="342" alt="INET" src="https://github.com/user-attachments/assets/2130dc3d-305c-47e2-9111-3c2ea6d2bd74" />

## Objective
Simulate an external (internet) network and configure connectivity between the internal enterprise network and external services such as DNS and web servers.


## Overview
I will use this external network  to represent the internet. This includes an Internet router, a switch, and public-facing services such as DNS and web servers. 

## Topology Overview

### Enterprise to Internet Connections

| Device        | Interface | Connected To | Interface |
|--------------|----------|--------------|----------|
| Router1      | G1/1/1   | INET-R1      | G1/0     |
| Router2      | G1/1/1   | INET-R1      | G2/0     |
