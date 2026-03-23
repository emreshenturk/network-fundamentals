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

### Simple Example
- Assume we have a host at `172.16.0.1`.
- `176.31.255.255` is a directed broadcast address for the `176.31.0.0/16` network.

If a router allows directed broadcasts, one packet can be delivered to many hosts in the target network.