# OpenVPN Tunnel – Secure Remote Access

## 🔐 Purpose

Access my home lab securely while traveling or working remotely.

## 🌐 OpenVPN Details

- **VPN Type**: Remote Access (SSL/TLS)
- **Authentication**: User-based login
- **Port**: 1194 UDP
- **Tunnel Network**: 192.168.50.0/24
  
## 🧰 Setup Steps

1. Enabled OpenVPN service on pfSense
2. Created user accounts + certificates
3. exported `.ovpn` files
4. Port-forwarded 1194 UDP from WAN to pfSense
5. Configured OpenVPN client on phone/laptop

## 📁 Files

- [`openvpn-client-config.ovpn`](config/opvn.md)]: Anonymized sample client config
