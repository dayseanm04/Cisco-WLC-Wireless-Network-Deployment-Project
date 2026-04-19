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

## Step 2: configure MGNT -C
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

<img width="993" height="531" alt="4" src="https://github.com/user-attachments/assets/8207fa6f-8549-490a-ac39-1cb889636457" />

- Click **Next**

## Step 6: RF Parameter Optimization

<img width="999" height="623" alt="5" src="https://github.com/user-attachments/assets/cb573db4-50ec-4b83-99c1-b13937051e22" />

- Leave RF settings as default
- Click **Next**

## Step 7: Finalize Configuration

<img width="927" height="653" alt="6" src="https://github.com/user-attachments/assets/5784c5f7-fc94-4a8c-8f2c-ad8e23e95413" />

- Review settings
- Click **Apply**

<img width="661" height="374" alt="7" src="https://github.com/user-attachments/assets/b83bfe08-6e53-480e-9aff-9492e818ea52" />

- Click **OK** when prompted

<img width="754" height="497" alt="8" src="https://github.com/user-attachments/assets/bfd686df-23e9-408c-9b20-6752637f8eb3" />

You will see this page for a minute, its not going to reboot.

Close the browser

## step 8: Access the WLC1 from MGNT-PC

- Mavigate to **https:192.168.50.254**
- Log in using the credentials created earlier
- Username: admin10
- Password: Pass123

<img width="908" height="514" alt="9" src="https://github.com/user-attachments/assets/3b21aaca-607f-424d-bad1-80a16385f019" />
<img width="1190" height="560" alt="10" src="https://github.com/user-attachments/assets/bfbaed17-33f0-41ff-a0b4-1d4e052240ad" />

