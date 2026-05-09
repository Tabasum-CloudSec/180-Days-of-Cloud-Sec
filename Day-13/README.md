# Day 13: Networking Journey - Playing the "Villain"
## SOHO Network Penetration Testing & Hardening

### 🔍 Overview
For Day 13, I transitioned from theory to practice by simulating a real-world attack on my own **SOHO (Small Office/Home Office)** network. By setting up a hacking server in the cloud, I was able to view my home network from the perspective of an external threat actor.

---

### 🛡️ Phase 1: The Attack (Gathering Intel)
The first step was to identify the "Digital Front Door"—the Public IP address.

* **Tool Used:** `Nmap` (Network Mapper) via a Linux Cloud Server.
* **Method:** Performed a perimeter scan to "knock" on every port.
* **The Goal:** To identify exposed services like **SSH (Port 22)** or **HTTP (Port 80)** that were left wide open to the world.

### ⚠️ Phase 2: The Danger Zone (IoT & Routers)
My scan revealed that "chatty" IoT devices and default configurations are the weakest links. 

**The 3 Biggest Risks Identified:**
1.  **Default Credentials:** Using `admin/admin` or `admin/password` is a hacker's best friend.
2.  **UPnP (Universal Plug and Play):** A protocol that opens ports automatically without user awareness.
3.  **Outdated Firmware:** Missing patches means practicing "hope-based security" rather than proactive defense.

---

### 🛠️ Phase 3: The Defense (Actionable Hardening)
After identifying the holes, I implemented 4 critical steps to harden the network perimeter:

| Step | Action Taken | Why? |
| :--- | :--- | :--- |
| **1** | **Disable UPnP** | Prevents apps from creating "hidden" holes in the firewall. |
| **2** | **VLAN Segmentation** | Isolated IoT devices (fridges, bulbs) onto a separate Guest Network. |
| **3** | **Update Everything** | Set the router to auto-update firmware to stay ahead of exploits. |
| **4** | **Use a VPN** | Stopped exposing individual ports; all remote access now goes through a secure tunnel. |

---

### 📝 Key Takeaway
> "Most home networks are basically a digital front door with the keys left in the lock." 

True security comes from reducing the **Attack Surface** and ensuring that even if one device is compromised (like a smart bulb), the rest of the network remains isolated and safe.

#CyberSecurity #Networking #EthicalHacking #HomeLab #Nmap #Linux #InfoSec #Day13 #SOHO #TechTips
