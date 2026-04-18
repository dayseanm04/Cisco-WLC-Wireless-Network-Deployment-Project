# 01-Validate-DHCP-IP-Assignment-on-Client-Devices

## Objective
Verify that client devices successfully obtain IP addresses from the DHCP server within their respective VLANs.

## Test Devices

| Device   | VLAN | Department        | Expected Result                  |
|----------|------|------------------|---------------------------------|
| HR-PC1 and 2   | 10   | Human Resources   | Receives IP from DHCP scope     |
| A-PC1  and 2  | 20   | Administration    | Receives IP from DHCP scope     |
