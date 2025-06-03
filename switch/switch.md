# VLAN Setup – Managed Switch (L2)
Intervlan routing handled by the router

## 🎯 Objective

Segment network traffic into isolated VLANs to improve security and manageability. 

## 💡 VLAN Design

| VLAN ID | Purpose          | Subnet          | Notes                  |
|---------|------------------|-----------------|-------------------------|
| 10      | Management       | 192.168.10.0/24 | For managing switch/router |
| 20      | Wireless Guest   | 192.168.20.0/24 | Guest Wi-Fi, restricted access |
| 30      | Iot Devices      | 192.168.30.0/24 | Cameras |
| 40      | Virtual Machines | 192.168.40.0/24 | Cybersecurity labs |

## ⚙️ Configuration Steps

1. Created VLANs on the switch CLI.
2. Assigned ports as access/trunk depending on usage
3. Tagged VLANs where trunking on pfSense port 
4. Verified connectivity and isolation with ping tests

## 📝 Example CLI

vlan database
vlan 10,20,30,40
exit

interface range gi1/0/2
switchport mode access
switchport access vlan 20
exit
