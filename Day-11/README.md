```markdown
# Day 11: Linux Web Services & Enterprise Network Architecture

## 🚀 Overview
Today’s learning focused on the intersection of Linux administration and large-scale networking. I explored how to deploy instant web services and analyzed the structural designs that power modern data centers.

---

## 🐧 Linux Lab: Instant Web Hosting
In a lab or penetration testing environment (like Hack The Box), speed is essential. I practiced using Python's built-in modules to host files without the overhead of a full web server stack.

### 1. Starting the Server
Using a single command to turn any directory into a network-accessible location:
```bash
python3 -m http.server 8000
```
* **Port Awareness:** Learned how to change the port (e.g., `8080`, `9000`) to avoid conflicts or bypass basic filters.
* **Use Case:** Rapidly transferring scripts or tools between machines.

### 2. Analyzing Traffic with `curl`
Moving beyond the browser to see the "raw" side of the web using the Command Line Interface (CLI).
```bash
curl -v http://localhost:8000
```
* **HTTP Headers:** Inspected the "handshake" metadata (Status codes, Content-Type, Server info).
* **Verbosity:** Used the `-v` flag to debug the request/response cycle.

---

## 🏗️ Networking: Enterprise & Data Center Design
Understanding how physical hardware is organized to handle massive traffic loads.

### 🏛️ Traditional 3-Tier Hierarchy
Used primarily in **Campus/Office** environments:
1.  **Core Layer:** The high-speed backbone.
2.  **Distribution Layer:** Policy-based connectivity and routing.
3.  **Access Layer:** Where end-devices (PCs, Printers) physically connect.

### 🌿 Modern Spine-Leaf Architecture
The gold standard for **Data Centers**:
* **Full Mesh:** Every Leaf switch connects to every Spine switch.
* **East-West Traffic:** Optimized for server-to-server communication.
* **Predictable Latency:** Every destination is exactly two hops away.

---

## 📊 Comparison Table

| Feature | 3-Tier Design | Spine-Leaf Design |
| :--- | :--- | :--- |
| **Primary Use** | Campus / Office Buildings | Modern Data Centers / Cloud |
| **Traffic Flow** | North-South (User to Web) | East-West (Server to Server) |
| **Scalability** | Vertical (Bigger switches) | Horizontal (Add more switches) |
| **Redundancy** | Spanning Tree Protocol (STP) | Equal-Cost Multi-Path (ECMP) |

---

## 🛠️ Tools Used
* **OS:** Linux (Ubuntu)
* **Environment:** Hack The Box Labs
* **Commands:** `python3`, `curl`, `cd`, `ls`, `mkdir`

---
*Created by [@tabasum.sec](https://www.instagram.com/tabasum.sec)*
```
