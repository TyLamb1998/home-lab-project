# 🏠 Home Lab Project – Cybersecurity & Networking

This project documents the design and configuration of my personal home lab, built to simulate enterprise network environments and explore real-world cybersecurity concepts.

## 🔍 Overview

My lab includes:
- A **pfSense** firewall/router for advanced networking and security
- A **managed switch** with VLANs for network segmentation
- **Remote VPN access** via OpenVPN
- Simulated access points, clients, and monitoring setups

## 📂 Lab Structure

| Component | Description |
|----------|-------------|
| [`Switch`](switch/switch-l2-setup) | Cisco Switch configuration and VLAN setup |
| [`pfsense`](pfsense/pfsense-Router-Firewall) | pfSense router & firewall rules, NAT, DNS, and more |
| [`VPN`](vpn/) | OpenVPN tunnel setup, configs, certificates, .ovpn files |
| [`docs`](docs/) | Overall architecture and design notes |

## 🚀 Goals

- Learn network segmentation, VLANs, and L2/L3 concepts
- Simulate perimeter security with pfSense
- Establish secure remote access

---

📌 **Note:** This lab runs on real hardware, but all configurations are anonymized and documented for public review.
