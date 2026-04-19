# 01 WLC Initial Configuration and Management Setup

## Objective
Perform the initial configuration of the Wireless LAN Controller (WLC1), including management interface setup and system settingsk.

## Reference Topology

<img width="869" height="448" alt="TFR" src="https://github.com/user-attachments/assets/c666670d-0315-458a-b806-cd17b8a8669e" />

## Step 1: Configure WLC1 management IP
- clicked on **WLC1**
- Click **Config**
- Click **Management**
- Configure Management IP, subnet mask and default gateway.
<img width="734" height="306" alt="WLC-MGNT" src="https://github.com/user-attachments/assets/7015a615-d783-4298-80cc-1a92e8d09326" />

## Step 2: Access the WLC1 from MGNT-PC
Note: MGNT-PC must be in the same subnet as WLC1

- Configure MGNM-PC1 IP address
- Click on **Desktop**
- Click on **IP config**

<img width="735" height="287" alt="MGNT-PC-IP" src="https://github.com/user-attachments/assets/ccb442d7-f428-4c7e-9fa8-041bab8bf122" />

- Exit IP config and click on **Web Browser**
- Navigate to **http:192.168.50.254**

Note: I might say request timed out, just close the browser and redo it!

## Step 3: Create Admin Credentials

| Setting        | Value    |
|----------------|----------|
| Username       | admin10  |
| Password       | Pass123  |

- Click **Start**

---

## Step 3: Configure System Settings

<img width="1059" height="558" alt="2" src="https://github.com/user-attachments/assets/dfe74e88-022c-46f3-83c4-51dbb1ee6a4d" />
- Click **Next**

## Step 4: Configure Management Interface

<img width="1055" height="600" alt="3" src="https://github.com/user-attachments/assets/5fdd2ef5-01fc-4d4a-93f7-ca97385c842e" />

- Click **Next**

Note: The default gateway is the SVI I configured on the **SW1** for VLAN 50.

## Step 5: Configure Wireless Network (WLAN)



