# OSI Model

| Layer | Name |
| --- | --- |
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |

| OSI Layer(s) | TCP/IP Layer |
| --- | --- |
| Application, Presentation, Session | Application |
| Transport | Transport |
| Network | Internet |
| Data Link, Physical | Network Access (Link) |

| OSI Model | TCP/IP Model | Hybrid Model |
| --- | --- | --- |
| 7. Application | Application | Application |
| 6. Presentation | Application | Application |
| 5. Session | Application | Application |
| 4. Transport | Transport | Transport |
| 3. Network | Internet | Network |
| 2. Data Link | Network Access (Link) | Data Link |
| 1. Physical | Network Access (Link) | Physical |

| PDU | Layer | Example / Protocol |
| --- | --- | --- |
| Data | Application | HTTP, HTTPS, FTP, Telnet |
| Segment | Transport | TCP/UDP |
| Packet | Network | IPv4, IPv6 |
| Frame | Data Link | Ethernet (MAC) |
| Bits | Physical | Bits |

| Encapsulation Stage | PDU | Added Header / Trailer | Result |
| --- | --- | --- | --- |
| 1 | Data | - | Application data |
| 2 | Segment | L4: TCP/UDP header | Data + TCP/UDP header |
| 3 | Packet | L3: IPv4/IPv6 header | Segment + IP header |
| 4 | Frame | L2: Ethernet header + trailer (FCS) | Packet + Ethernet header/trailer |
| 5 | Bits | - | 0 and 1 on physical media |