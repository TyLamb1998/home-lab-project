# VLAN Setup – Managed Switch 
Intervlan routing handled by the router

## 🎯 Objective

Segment network traffic into isolated VLANs to improve security and manageability. 

## 💡 VLAN Design

| VLAN ID | Purpose          | Subnet          | Notes                  |
|---------|------------------|-----------------|-------------------------|
| 10      | Management       | 192.168.10.0/24 | For managing switch/router |
| 20      | Wireless Guest   | 192.168.20.0/24 | Guest Wi-Fi, restricted access |
| 30      | Virtual Machines | 192.168.30.0/24 | Cybersecurity labs |

## ⚙️ Configuration Steps

1. Created VLANs on the switch CLI.
2. Assigned ports as access/trunk depending on usage
3. Tagged VLANs where trunking on pfSense port (Router on a stick) 
4. Verified connectivity and isolation with ping tests

## 📝 Example CLI

vlan database
vlan 10,20,30
exit

interface gi1/0/2
 description Wireless AP
 switchport mode access
 switchport access vlan 20
 spanning-tree portfast
 power inline auto
 exit
