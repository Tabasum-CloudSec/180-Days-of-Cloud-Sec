# Day 4: Networking Infrastructure & Data Flow 🌐

## Objective
To understand the physical and logical path data takes from a local device to the global internet, identifying key security touchpoints.

## The Infrastructure Chain
Today I mapped the hardware flow:
1. **PC (Origin):** The starting point of the data packet.
2. **Switch:** Connecting devices within the local area network (LAN).
3. **Router:** The gateway that routes traffic between different networks.
4. **Firewall:** The primary security layer that filters incoming/outgoing traffic.
5. **Modem/Fiber:** The translator that connects the local network to the ISP via light signals.

## Why this matters for Cloud Security
Security isn't just about software; it's about the "road" the data travels on. By understanding this flow, I can better understand where to implement:
- Access Control Lists (ACLs)
- Packet Filtering
- Network Address Translation (NAT)

> **Status:** Networking Fundamentals - Part 1 Complete.
