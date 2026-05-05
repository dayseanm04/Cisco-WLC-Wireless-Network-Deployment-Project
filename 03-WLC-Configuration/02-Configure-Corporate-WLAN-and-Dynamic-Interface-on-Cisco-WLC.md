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


