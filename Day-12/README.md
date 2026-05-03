# 🌐 CCNA 200-301 | Day 12: WAN Fundamentals

## 📌 Overview
Shifting focus from **LAN (Local Area Network)** to **WAN (Wide Area Network)**. While LANs operate within a single geographical location under private ownership, WANs connect dispersed LANs across cities or countries via Service Providers.

---

## 🛠️ WAN Architecture & Terminology
Understanding the physical and logical boundaries between the Customer and the ISP.

| Term | Full Name | Definition & Responsibility |
| :--- | :--- | :--- |
| **CPE** | **Customer Premises Equipment** | Hardware located at the subscriber's site (Routers, WAPs). **[User Owned]** |
| **Demarc** | **Demarcation Point** | The physical point where ISP responsibility ends and CPE begins. |
| **CO** | **Central Office** | The ISP facility where the local loop connects to the provider's switching center. |



---

## 🏗️ Modern WAN Connectivity Menu
A breakdown of how modern enterprises bridge the gap between branches.

### **1. Dedicated Leased Lines**
* **Protocol:** T1/E1, T3/E3.
* **Pros:** Point-to-point, 100% private, guaranteed bandwidth.
* **Cons:** Extremely expensive, difficult to scale.

### **2. Metro Ethernet (MetroE)**
* **Nature:** Extending Layer 2 Ethernet over the WAN.
* **Pros:** High speed (up to 100Gbps), familiar Ethernet protocols, cost-effective.
* **Best Use:** Connecting offices within a metropolitan area.

### **3. MPLS (Multiprotocol Label Switching)**
* **Layer:** Often called **"Layer 2.5"**.
* **Mechanism:** Forwards data based on **Labels** rather than IP addresses.
* **Architecture:** Supports Any-to-Any connectivity (Full Mesh).

---

## 🔐 Public WAN (The Internet)
Using the Public Internet as a cost-effective WAN solution requires encryption to maintain security.

* **Site-to-Site VPN:** Creates a secure "Tunnel" across the public internet.
* **Encapsulation:** Uses **IPsec** to encrypt data packets.
* **Trade-off:** Lower cost but **No Quality of Service (QoS)** guarantees.
