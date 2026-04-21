# Day 8: OSI Model & Linux Daemons 🛡️

## 📍 Overview
Today's focus was on the "Invisible" layers of the cloud: how data is packaged at the network level and how Linux handles that data using background processes called Daemons.

---

## 📦 1. Networking: The OSI Assembly Line
I learned that data isn't just "sent"; it is encapsulated in layers.

| Layer | Name | What Happens? |
| :--- | :--- | :--- |
| **Layer 7** | Application | The interface (Browser/SSH client). |
| **Layer 6** | Presentation | Data formatting & **Encryption (SSL/TLS)**. |
| **Layer 4** | Transport | Delivery method choice: **TCP** (Reliable) vs **UDP** (Fast). |
| **Layer 3** | Network | IP Addressing (Finding the right "House"). |

### TCP vs UDP
- **TCP:** Uses a **3-Way Handshake** (SYN -> SYN-ACK -> ACK) to ensure 100% reliability.
- **UDP:** Focuses on speed; no handshake, just sending data (best for live video).

---

## 👻 2. Linux: The Power of Daemons
Daemons are background processes that keep a server running.
- **Naming:** Usually end in `d` (e.g., `sshd`, `httpd`).
- **Function:** They "listen" on specific **Ports**.
- **Example:** When a packet hits **Port 22**, the `sshd` daemon wakes up to handle the secure login.

### Useful Commands Used:
- `systemctl status <daemon>`: Check if a "ghost" is active.
- `ps -ef | grep <daemon>`: View the process running in the background.

---

## 🛡️ Cloud Security Connection
By understanding which **Daemons** are running on which **Ports**, we can secure a cloud server by:
1. Closing all unused ports (Layer 4).
2. Ensuring only encrypted traffic (Layer 6) is accepted.
3. Monitoring active daemons for suspicious behavior.

---
*Follow my daily progress on Instagram: [@tabasum.sec]*
