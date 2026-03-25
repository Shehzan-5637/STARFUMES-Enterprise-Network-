# STARFUMES-Enterprise-Network-
Cisco Packet Tracer simulation of a small enterprise network for STARFUMES, demonstrating LAN/WAN segmentation, DHCP, DNS, and inter-subnet routing.

# 🌐 STARFUMES Small Enterprise Network – Cisco Packet Tracer

A simulated **Small Enterprise Network** for STARFUMES, designed in **Cisco Packet Tracer**, demonstrating real-world LAN/WAN segmentation, DHCP/DNS configuration, and inter-subnet routing for a small-to-medium enterprise (SME).

---

## 📌 Project Overview

This project models a realistic enterprise network connecting:

- **Head Office LAN (Corporate Services)**
  - Dedicated servers: DHCP, DNS, Web
  - Internal staff devices
- **Client LAN (End-Users)**
  - PCs, laptops, smartphones
  - Wireless Access Point (AP) integration
- **WAN Backbone**
  - Cloud/ISP simulation connecting both networks

The project demonstrates:

- Network segmentation
- Automated IP addressing via DHCP
- Name-based service access (DNS)
- Inter-LAN connectivity and routing

---

## 🎯 Motivation

To gain hands-on experience in designing, configuring, and verifying a multi-site enterprise network using Cisco Packet Tracer while simulating a secure, functional environment where internal corporate services are separated from general client access.

---

## 📝 Concept / Problem Statement

Design and implement a small enterprise network with:

1. **Network Segmentation:** Two subnets
   - Head Office: `192.168.1.0/24`
   - Client Network: `192.168.2.0/24`
2. **Automated Addressing:** DHCP for all end devices
3. **Inter-VLAN/Subnet Routing:** Full IP connectivity across subnets
4. **Web and DNS:** Access the Web Server using the domain name `starfumes`

---

## 🏗️ Design & Architecture

**Head Office LAN (192.168.1.0/24)**

- **Equipment:** Switch, Router, Servers (DHCP, DNS, Web)  
- **IP Assignments:**
  - Router (Gig0/0): `192.168.1.5`
  - DHCP Server: `192.168.1.1`
  - DNS Server: `192.168.1.2`
  - Web Server: `192.168.1.3`
- **Services:** DHCP, DNS mapping (`starfumes → 192.168.1.3`), Web server

**Client LAN (192.168.2.0/24)**

- **Equipment:** PCs, Laptops, Smartphones, Router, AP, DSL Modem  
- **IP Assignments:** Dynamic via DHCP; Client Router (Gig0/0): `192.168.2.2`

**WAN Backbone (192.168.3.0/24)**

- **Connection:** Head Office ↔ Cloud ↔ Client LAN  
- **IP Assignments:**  
  - Head Office Router (Gig0/1): `192.168.3.1`  
  - Client DSL Modem: `192.168.3.2`  

**Routing:** Static or dynamic routing between subnets to ensure full connectivity.

---

## 🛠️ Implementation / Methodology

1. **Device Placement & Wiring**
   - Switches, routers, servers, and clients connected according to topology
   - Cable types: straight-through / crossover as appropriate

2. **Head Office Server Configuration**
   - DHCP pool setup for staff devices
   - DNS server mapping `starfumes → 192.168.1.3`
   - Web server setup (simple HTML page)

3. **Router Configuration**
   - Assign LAN/WAN IPs
   - Configure static routes to remote subnets

4. **Client Configuration**
   - PCs, laptops, and smartphones set to receive DHCP IPs

5. **Testing & Verification**
   - Ping between subnets (Layer 3)
   - Access web server via IP & `starfumes` domain
   - Verify DHCP and DNS functionality

---

## 📊 Verification / Test Results

| Test Origin        | Test Destination         | Protocol | Expected Result | Observed Result |
|-------------------|------------------------|----------|----------------|----------------|
| Client PC 192.168.2.x | Head Office PC 192.168.1.x | PING     | Success        | Success        |
| Client PC 192.168.2.x | Web Server 192.168.1.3    | HTTP     | Success        | Success        |
| Client PC 192.168.2.x | Web Server `starfumes`    | DNS/HTTP | Success        | Success        |

---

## 🔍 Analysis

- **Routing Success:** Layer 3 connectivity verified between subnets
- **DHCP Operation:** Dynamic IP assignment worked for all clients, including wireless devices
- **DNS Validation:** Clients successfully accessed `starfumes` via DNS  
- **Security & Segmentation:** Corporate services are isolated from client access, ready for future ACLs

---

## ✅ Deliverables Achieved

1. DHCP functional on all devices  
2. Successful inter-subnet ping connectivity  
3. Web service accessible via IP and domain name  
4. DNS resolution confirmed

---

## 🛠️ Tools / Technologies

- **Cisco Packet Tracer** – network simulation  
- Networking protocols: DHCP, DNS, ICMP, HTTP  
- IP addressing and subnetting

---

## 📈 Future Improvements

- ACLs for enhanced security  
- VLAN segmentation for more granular control  
- VPN simulation for remote client access  
- Integration with real-world servers for hybrid simulation

---

## 📫 Contact

**Ali Shehzan Punjwani**  
🎓 BSCS Student @ Iqra University  
📍 Karachi, Pakistan  
📧 shehzansohail5637@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/ali-shehzan-punjwani)
