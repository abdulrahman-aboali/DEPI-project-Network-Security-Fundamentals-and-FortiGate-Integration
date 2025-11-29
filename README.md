📡 FortiGate HQ & Branch Network Project
A practical implementation project focusing on secure enterprise network design using FortiGate firewalls, VLAN segmentation, NAT, routing, and IPSec VPN.
---
🛠️ Project Overview
- 🔥 Implement firewall policies and NAT
- 🧱 VLAN segmentation (HQ & Branch)
- 🚦 Static routing between firewalls
- 🔐 IPSec site‑to‑site VPN
- 🏗️ Inter‑VLAN routing with core switches

---
🧩 Network Architecture
- 🏢 Two FortiGate firewalls: **HQ & Branch**
- 🔌 Core + Access switches
- 🌐 Simulated WAN network
- 🛡️ IPSec VPN tunnel for secure communication

---
🌐 IP Addressing Scheme
🏛️ HQ VLANs
• VLAN 10 → 192.168.10.0/24
• VLAN 20 → 192.168.20.0/24
• VLAN 30 → 192.168.30.0/24
• VLAN 40 → 192.168.40.0/24

🔌 HQ Firewall Interfaces
• port1 (WAN): 192.168.192.250/24
• port2 (MGMT): 10.10.10.20/24
• port3 (Internal): Connected to core switch

🏢 Branch VLANs
• VLAN 10 → 192.168.11.0/24
• VLAN 20 → 192.168.21.0/24
• VLAN 30 → 192.168.31.0/24
• VLAN 40 → 192.168.41.0/24

🔌 Branch Firewall Interfaces
• port1 (WAN): 192.168.192.251/24
• port2 (MGMT): 10.10.10.21/24
• port3 (Internal): Connected to branch core switch

---
🚦 Routing Configuration
• HQ Default Route → 192.168.192.2 (ISP Gateway)
• Branch Default Route → 192.168.192.2
• Internal VLANs routed over IPSec tunnel

---
🧱 Firewall Policies & NAT
🏛️ HQ Firewall
• VLANs → WAN NAT Enabled
• IT VLAN (40) uses IP Pool: 192.168.192.100–192.168.192.150

🏢 Branch Firewall
• VLANs → WAN NAT Enabled
• IT VLAN (40) uses IP Pool: 192.168.192.151–192.168.192.200

---
🔐 IPSec VPN (Site-to-Site)
A secure IPSec VPN tunnel connects HQ and Branch to allow encrypted communication between internal VLAN networks.

---
🧪 Testing & Validation
• IT VLAN internet access ✔️
• HR VLAN blocked from internet ✔️
• HQ ↔ Branch HR ping successful ✔️
• All devices can reach gateway (192.168.192.2) ✔️

---
🏁 Final Notes
This project demonstrates secure, scalable, and structured network deployment using FortiGate firewalls and Cisco switching. The configuration ensures proper segmentation, security enforcement, and VPN-based inter-branch communication.

---
🧑‍💻 Team Members
Abdulrahman Badr Metwaly
Mustafa Hesham Elkolaly
Abdulrahman Mohamed Kamel
Abdelwahab Nabil Zakaria
Mustafa Abdelhady Mohammed

