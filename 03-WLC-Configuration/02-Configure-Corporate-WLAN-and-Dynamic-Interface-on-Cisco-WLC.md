# Configure Corporate WLAN and Dynamic Interface on Cisco WLC

## Objective
Configure a wireless network for the enterprise on the Wireless LAN Controller (WLC1). This includes configuring dynamic interface, IP , and mapping the interface to the WLAN.

## Reference Topology

<img width="896" height="447" alt="TFR" src="https://github.com/user-attachments/assets/983958d9-e25e-47b4-860f-577488f874e1" />

## Cconfigure dynamic interface for the corporate WLAN

### Access the WLC1 on MGNT-PC

- Click on MGNT-PC
- Click on Desktop
- Browser
- Navigate to **https ://192.168.50.254**
- Login 

<img width="1244" height="646" alt="1" src="https://github.com/user-attachments/assets/2c7cdf08-3dd1-4364-ba15-3fb15d0beced" />


### Create a dynamic interface
- Click on **CONTROLLER**

<img width="1242" height="545" alt="2" src="https://github.com/user-attachments/assets/4d203b1e-fdc0-4a3f-8a1a-79e1eb9d8010" />

- Click on **Interfaces**

<img width="1242" height="473" alt="3" src="https://github.com/user-attachments/assets/91792db6-d8e7-4b0e-a110-10cb28147f43" />

- Configured the following:
- **Interface Name**: corp-wifi
- **VLAN ID**: 500
- Click **Apply**

<img width="1211" height="468" alt="4" src="https://github.com/user-attachments/assets/7e163dbe-0d32-41ea-8d7a-9dea884c7196" />

### Configure a dynamic interface

Configured the following:
- **Port id**: 1
- **IP address**: 172.16.1.10
- **Netmask**: 255.255.255.0
- **Default Gateway**: 172.16.1.1
- **DHCP Server**: 10.0.0.10
- Click **Apply** to save.

<img width="1192" height="754" alt="6" src="https://github.com/user-attachments/assets/5e214500-7140-4468-9783-8cb3784d519f" />

### Create the WLAN for the corporate-wifi
- Click on **WLANs**

<img width="1212" height="460" alt="7" src="https://github.com/user-attachments/assets/5a67b02d-ca40-40b1-97ae-41076579389c" />

- Click Go next to "**Create New**" on the top right
Configured the following:
- **Profile Name**: corp-wifi
- **SSID**: corp-wifi
- **ID**:: 1
- Click **Apply** to save

<img width="1218" height="476" alt="8" src="https://github.com/user-attachments/assets/b22d8abb-4af9-4278-a344-f79d0ff1ac63" />

<img width="1224" height="486" alt="10" src="https://github.com/user-attachments/assets/b2dc78b9-913e-4b0d-92c8-3e99117343d6" />

### Note: I will configure wireless security later!
