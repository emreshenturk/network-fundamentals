# What is an IP address?
An IP address is a **Layer 3 logical address** assigned by an administrator.

---

## IPv4 Address Classes (Legacy)

> These classes are an old model. Today, IPv4 networks are designed mostly with **CIDR**.

| Class | Traffic Type | Notes |
|---|---|---|
| A, B, C | Unicast | Used for one-to-one communication |
| D | Multicast | Used for one-to-many group communication |
| E | Reserved | Experimental / future use |

### Important Notes
- **IPv6** does not use address classes.
- IPv4 class-based addressing was replaced by **CIDR**.
- **IANA** = Internet Assigned Numbers Authority.

---

## Class A

### Rule
- First bit is always `0`.

### First Octet (Binary)
- Range: `0000 0000` to `0111 1111`

### Address Range
- Theoretical range: `0.0.0.0` to `127.255.255.255`
- Practical usable class range: `1.0.0.0` to `126.255.255.255`

### Network/Host View
- Example IP: `10.1.1.1`
- In Class A logic:
	- First octet (`10`) = **network** part
	- Remaining octets (`1.1.1`) = **host** part

## Quick Check
- `10.1.1.1` belongs to **Class A** (first octet is between `1` and `126`).
- First bit of `10` in binary is `0` (`00001010`), so it matches Class A.

---

## Class B
### First Octet (Binary)
- Range: `1000 0000` to `1011 1111`

### Address Range
- Range: `128.0.0.0` to `191.255.255.255`

### Network/Host View
- Example IP: `172.16.1.1`
- In Class B logic:
	- First 2 octets (`172.16`) = **network** part
	- Remaining 2 octets (`1.1`) = **host** part

---

## Class C
### First Octet (Binary)
- Range: `1100 0000` to `1101 1111`

### Address Range
- Range: `192.0.0.0` to `223.255.255.255`

### Network/Host View
- Example IP: `192.168.1.1`
- In Class C logic:
	- First 3 octets (`192.168.1`) = **network** part
	- Remaining 1 octet (`1`) = **host** part

---

## Class D (Multicast)
### First Octet (Binary)
- Range: `1110 0000` to `1110 1111`

### Address Range
- Range: `224.0.0.0` to `239.255.255.255`

---

## Class E

### First Octet (Binary)
- Range: `1111 0000` to `1111 1111`

### Address Range
- Range: `240.0.0.0` to `255.255.255.255`

---

## Directed Broadcast Address

### What It Means
A directed broadcast is a packet sent to the **broadcast address of a specific remote network**.

### How to Find It
1. Start with the target network (example: `176.31.0.0/16`).
2. Keep the network part the same (`176.31`).
3. Set all host bits to `1`.
4. Result: `176.31.255.255` (directed broadcast for that network).

### Example
- Source host: `172.16.0.1`
- Target network: `176.31.0.0/16`
- Directed broadcast address: `176.31.255.255`

If a router forwards directed broadcasts, one packet can be replicated to many hosts in the destination network.

---

- This mechanism was abused in old amplification attacks (for example, Smurf).
- Because of that, most routers block directed broadcasts by default.
- In real networks, keep this feature disabled unless there is a strict operational requirement.

## Local Loopback Address

### What It Is
Loopback addresses let a device send traffic to **itself**.

### IPv4 Loopback
- Reserved block: `127.0.0.0/8`
- Full range: `127.0.0.0` to `127.255.255.255`
- Most common host address: `127.0.0.1`

### IPv6 Loopback
- Address: `::1/128`

### Why It Is Used
- Test TCP/IP stack on the local machine.
- Test local services without using the physical network.

### Note
- These addresses are intentionally reserved for local testing.
- They are not usable as normal routed host addresses on the Internet.