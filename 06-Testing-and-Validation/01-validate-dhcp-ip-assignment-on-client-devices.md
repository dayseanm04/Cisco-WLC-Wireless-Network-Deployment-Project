# 01-Validate-DHCP-IP-Assignment-on-Client-Devices

## Objective
Verify that client devices successfully obtain IP addresses from the DHCP server within their respective VLANs.

## Test Devices

| Device   | VLAN | Department        | Expected Result                  |
|----------|------|------------------|---------------------------------|
| HR-PC1 and 2   | 10   | Human Resources   | Receives IP from DHCP scope     |
| A-PC1  and 2  | 20   | Administration    | Receives IP from DHCP scope     |

### Step 1: Verify IP Assignment

Verify the assigned IP configuration: 

### On HR-PC1 ipconfig /renwew

<img width="735" height="309" alt="HR1" src="https://github.com/user-attachments/assets/e7833299-6f9e-46a8-815f-3149cae7985f" />

### On HR-PC2

<img width="734" height="304" alt="HR2" src="https://github.com/user-attachments/assets/056ccfc7-b560-44b6-a1fc-f57acf861ec3" />
 ipconfig /renwew

### On A-PC1 ipconfig /renwew

<img width="739" height="317" alt="A1" src="https://github.com/user-attachments/assets/f4ca3546-eb4f-4a6a-96ca-45ed0ca4afdb" />

### On A-PC2

<img width="739" height="314" alt="A2" src="https://github.com/user-attachments/assets/df088ee9-c77a-44ee-ba56-861bcf93e2ba" />
 ipconfig /renwew

## Validation Checklist

- Client receives an IP address within the correct subnet. [**DHCP Scopes reference**](../04-Implementation/Network-Services/01-configure-dhcp-scopes-for-vlans.md)
- Default gateway matches the VLAN SVI. [**VLAN and SVI Configuration**](../01-Setup/02-VLAN-and-SVI-Configuration.md)








