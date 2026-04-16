# 03 LACP etherchannel configuration

## Objective
Configure Layer 3 EtherChannel links using LACP to provide redundancy between network devices.

## Overview
EtherChannel bundles multiple physical interfaces into a single logical link . In this design, Layer 3 EtherChannels are used between routers and switches to provide redundancy high availability.

## EtherChannel Summary
| Connection        | Port-Channel | Subnet           | Device A IP     | Device B IP     |
|-------------------|---------------|------------------|----------------|----------------|
| Router1 ↔ Router2 | Po1         | 10.20.10.0/30    | 10.20.10.1      | 10.20.10.2      |
