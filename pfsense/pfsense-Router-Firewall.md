
# pfSense Firewall Rules

## 🔐 Objective

Create a secure firewall ruleset that enforces least privilege across VLANs.

## 🧱 Key Rules


| VLAN       | Internet | LAN Access         | Notes                                           |
|-------------------|-----------|--------------------|-------------------------------------------------|
| **10 (Mgmt)**     | ✅ Yes   | ✅ Yes             | Full access to everything                      |
| **20 (Wireless)** | ✅ Yes   | ❌ No              | ❗ Exception: 1 phone allowed to LAN            |
| **30 (VMs)**      | ✅ Yes   | ✅ Yes             | Full access for test VMs             |
| **40 (VPN)**      | ✅ Yes   | ✅ Yes             | Full remote access (LAN + VLANs)               |

- 🔒 Inter-VLAN traffic is **blocked by default** unless explicitly allowed.
# 🛡️ Home Network Firewall Rules (Security-Hardened)

This document outlines the VLAN and firewall rule configuration for a secure home lab network.

## 🔑 VLAN Rules Summary

| VLAN | Description       | Internet | LAN Access            | Notes                                                             |
|------|-------------------|----------|-----------------------|-------------------------------------------------------------------|
| 10   | Management        | ✅       | ✅ (to all VLANs)    | Used for network admin; trusted systems only                      |
| 20   | Wireless          | ✅       | 🚫                   | Only allow specific MAC/IP (e.g., phone)                          |
| 30   | VM/Workstations   | ✅       | ✅ (Selective)       | Limit to certain ports/IPs                                        |
| 40   | VPN               | ✅       | ✅ (to all VLANs)    | Used to simulate remote trusted access                            |


## 🚫 Default Policy

- Block all inter-VLAN traffic unless explicitly allowed
- Allow outbound Internet by default (unless restricted)


## 🔁 NAT and Port Forwarding

| Rule | Description |
|------|-------------|
| NAT | Outbound NAT set to "hybrid" to allow VLANs to access WAN |
| Port Forward | OpenVPN port forwarded to pfSense from WAN |

## 🛠️ Rule Setup Process

1. Created alias groups for VLAN IP ranges
2. Applied firewall rules to each VLAN interface
3. Used pfSense’s logging and diagnostics to validate
