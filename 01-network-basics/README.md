**Host:** A host is an end system connected to a network (typically the Internet) that can send and receive data. Examples include computers, smartphones, and smartwatches.
**Server:** A server provides services or resources to clients over a network.

---
| Feature    | Physical Topology     | Logical Topology             |
| ---------- | --------------------- | ---------------------------- |
| Definition | Hardware arrangement  | Data flow and communication patterns |
| Visibility | Physically observable | Abstract (not directly visible) |
| Focus      | Cables and devices    | Protocols and data transmission |
 
---
**Hub:** Hubs are simple Layer 1 devices. They receive data on one port and forward it to all other ports.
**Bridge:** Bridges are Layer 2 devices that learn MAC addresses and forward frames only to the correct segment, unlike hubs. They perform this filtering and forwarding in software using the CPU.
**Switch:** Switches are similar to bridges but perform Layer 2 forwarding in hardware (ASICs), which provides much higher performance.
**Router:** A router is a Layer 3 device that forwards packets between different networks and typically provides Internet connectivity.
**Firewall:** A firewall is placed between network segments (for example, between a switch and a router or between a router and the Internet) to enforce security policies by allowing or blocking traffic.
**IDS (Intrusion Detection System):** Monitors network or host activity to detect suspicious behavior and generate alerts.
**IPS (Intrusion Prevention System):** Monitors traffic in line, detects malicious activity, and automatically blocks or mitigates it.