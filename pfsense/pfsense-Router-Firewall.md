
# pfSense Firewall Rules

## 🔐 Objective

Create a secure firewall ruleset that enforces least privilege across VLANs.

## 🧱 Key Rules

- **Block inter-VLAN traffic** by default
- **Allow VLAN 10** (management) to access all
- **Allow VLAN 20** (wireless) internet access, no LAN access 
- **Allow VLAN 30 (guest)** internet access, 
- **Allow VLAN 40** (vpn) full access to LAN

## 🔁 NAT and Port Forwarding

| Rule | Description |
|------|-------------|
| NAT | Outbound NAT set to "hybrid" to allow VLANs to access WAN |
| Port Forward | OpenVPN port forwarded to pfSense from WAN |

## 🛠️ Rule Setup Process

1. Created alias groups for VLAN IP ranges
2. Applied firewall rules to each VLAN interface
3. Used pfSense’s logging and diagnostics to validate
