# 🖧 Small Office/Home Office Network Design - Packet Tracer

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=flat&logo=cisco&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-IPv4%20%7C%20Subnetting%20%7C%20DHCP-0A66C2?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-2ea44f?style=flat)
![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=flat)
![Certificate](https://img.shields.io/badge/Cisco%20NetAcad-Networking%20Basics-1BA0D7?style=flat&logo=cisco&logoColor=white)

---

## 📌 Project Overview

This project simulates a **Small Office / Home Office (SOHO) network** designed for a 3-department organisation. Built entirely in **Cisco Packet Tracer**, it demonstrates real-world network segmentation, IP addressing, routing, and connectivity verification which are executed in the real world by entry-level network or IT support role.

---

## 🏢 Network Architecture

The network is divided into **3 departments**, each on its own subnet, connected through a central **Router1**.

| Department | Subnet | Switch | Devices |
|---|---|---|---|
| Admin / IT | `192.168.1.0/26` | Switch-AdminIT | 2× PC, 1× Laptop, 1× Printer |
| Finance / HR | `192.168.1.64/26` | Switch-FinanceHR | 2× PC, 1× Laptop, 1× Printer |
| Reception | `192.168.1.128/26` | Switch-Reception | 2× PC, 1× Laptop, 1× Printer |

**Total devices:** 1 Router · 3 Switches · 6 PCs · 3 Laptops · 3 Printers = **16 network nodes**

---

## 🗺️ Topology Diagram

![Network Topology](topology.png)

*Three colour-coded departments connected to a central router — Admin/IT (green), Finance/HR (blue), Reception (magenta)*

---

## ✅ Connectivity Tests

All inter-subnet and intra-subnet connectivity was verified from **PC1** using `ping` and `tracert`.

![Ping and Tracert Results](pinging_devices_pmg.png)

| Test | Source | Destination | Result |
|---|---|---|---|
| Intra-subnet ping | PC1 `192.168.1.x` | `192.168.1.2` | ✅ 0% packet loss |
| Cross-subnet ping | PC1 `192.168.1.x` | `192.168.1.190` (Reception) | ✅ 0% packet loss |
| Cross-subnet ping | PC1 `192.168.1.x` | `192.168.1.67` (Finance/HR) | ✅ 3/4 packets (caused by an arp delay which is normal behaviour and not due to any incorrect configuration) |
| Tracert | PC1 | `192.168.1.132` | ✅ 2 hops — confirms routing via Router1 |



---

## 📂 Repository Structure

```
📁 soho-network-packet-tracer/
│
├── 📄 README.md                          ← You are here
├── 🖧 building_1.pkt                     ← Cisco Packet Tracer source file
├── 🖼️  topology.png                      ← Full network topology screenshot
├── 🖼️  pinging_devices_pmg.png           ← Ping & tracert results screenshot
└── 📊 Packet_Tracer_Network_Project.xlsx ← Device inventory, subnet plan & test log
```

---

## 🔧 Concepts Demonstrated

This project covers the following topics from the **Cisco Networking Academy — Networking Basics** curriculum:

| Module | Concept Applied |
|---|---|
| Module 4 — Build a Home Network | Physical topology design, device placement |
| Module 7 — The Access Layer | Switch configuration, end-device connectivity |
| Module 8 — The Internet Protocol | IPv4 addressing for all 16 nodes |
| Module 9 — IPv4 & Network Segmentation | Subnetting into 3 `/26` networks from `192.168.1.0/24` |
| Module 11 — Dynamic Addressing with DHCP | DHCP pool configuration on router |
| Module 12 — Gateways to Other Networks | Default gateway assignment per subnet |
| Module 13 — The ARP Process | ARP delay observed in cross-subnet first-ping |
| Module 14 — Routing Between Networks | Inter-VLAN routing via router interfaces |
| Module 17 — Network Testing Utilities | `ping` and `tracert` for connectivity verification |

---

## 📊 Documentation

A structured Excel workbook is included with 4 sheets:

1. **Device Inventory** — IP, MAC, subnet, gateway, and role for every device
2. **Subnet Planning** — network addresses, CIDR, DHCP pool configuration
3. **Connectivity Test Log** — all ping/tracert results with pass/fail status
   
---

## 🎓 Certificate

This project was built as a practical demonstration of skills learned in the **Cisco Networking Academy — Networking Basics** course.

[![Cisco NetAcad](https://img.shields.io/badge/Cisco%20NetAcad-Networking%20Basics%20Certificate-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)](https://www.netacad.com)

> 📎 *https://www.credly.com/badges/c797a1fe-6573-4382-be5d-ecc73052ab15*

---

## 🚀 How to Open This Project

1. Download and install **Cisco Packet Tracer** for free at [netacad.com](https://www.netacad.com)
2. Clone or download this repository
3. Open `Final Build.pkt` in Packet Tracer
4. Explore the topology, click any device, and go to **Desktop → Command Prompt** to run your own ping tests

---

## 👤 Author

**Parth Soni**
First-year Computer Science Student
📍 Bhopal, India
🔗 https://www.linkedin.com/in/thatisparth/

---

*Built with curiosity and a lot of ping commands*
