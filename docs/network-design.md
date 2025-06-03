# 🔧 Home Lab Architecture

## 🖥️ Hardware Overview

  Network devies: pfSense FW/ Router, Cisco SG300 Switch,  Aruba Access Point
  Clients: Windows Laptop, Linux VMs, IoT devices 

## 🗺️ Network Layout

                            [Internet]
                                 |
                        [pfSense Router]    
                       /                \              
              [ Managed Switch ]     [Open Vpn]  
               /     |      \            |
        VLAN10     VLAN20   VLAN 40    VLAN 50
        MNGT     Wireless   VM's        VPN
