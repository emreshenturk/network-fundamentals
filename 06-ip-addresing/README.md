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

## Class A (Detailed)

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

---

## Quick Check
- `10.1.1.1` belongs to **Class A** (first octet is between `1` and `126`).
- First bit of `10` in binary is `0` (`00001010`), so it matches Class A.