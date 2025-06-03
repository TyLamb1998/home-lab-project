# 🛡️ Snort IDS/IPS Configuration on pfSense

## Overview

This section documents how I implemented Intrusion Detection and Prevention on my home network using **Snort** on **pfSense**. The goal is to enhance network security by monitoring traffic for suspicious activity and blocking known threats using a layered approach.

---

## 🔧 Implementation Details

### ✅ Rule Sets Enabled
- **Snort Community Rules**
- **Snort Subscriber Rules (Talos)**  
  _(Includes more advanced and timely threat signatures)_

> Rules are updated automatically on a regular schedule to ensure the latest protections.

---

### 🔍 False Positives Management

To maintain network usability and reduce unnecessary noise:
- I monitor Snort logs regularly.
- Any rule generating consistent false positives is investigated.
- If confirmed as benign, the rule is **disabled** to prevent future alerts.
- Logs are **stored** locally for audit and troubleshooting.

---

## 🗂️ Interface Deployment

Snort is enabled on the following pfSense interfaces:
- **WAN**: Monitors all incoming threats from the internet.
- **LAN** (trusted): Monitors internal behavior and east-west traffic.
-**layered detection**—catching both external threats and potential lateral movement.

---

## ✅ Future Improvements

- Implement automatic rule tuning or alert scoring.
- Integrate logs into a centralized SIEM (e.g., Splunk or ELK stack).
- Leverage custom alert rules for known false positive-prone devices.




