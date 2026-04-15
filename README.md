*This project has been created as part of the 42 curriculum by* **ɢᴏᴍᴀɴᴅᴀᴍ**.

## Description

**Net Practice** teaches TCP/IP addressing fundamentals through hands-on exercises. The objective is to understand how IP addressing, subnet masks, and routing decisions work in real networks.

Key concepts covered:
- Subnet masks and network segmentation
- Network/broadcast/host address ranges
- Default gateway routing behavior
- Direct communication vs. routed communication

### Core Networking Topics

- **IPv4 Addressing:** 32-bit addresses with CIDR notation and subnet masking
- **Routing:** Packets traverse networks and routers make forwarding decisions
- **Network Design:** Subnetting, address allocation, and host connectivity

---

## Instructions

### Setup

1. **Acquire** the NetPractice files from the 42-intranet
2. **Extract** into a folder, and apply **chmod +x** to **run.sh**
3. **Run** the training interface: **./run.sh** or similarly,
   ```bash
   chmod +x ./run.sh
   ```
   
### Completing Levels

- Work through **10 configuration levels**
- However, the evaluation starts at **level 06** onwards
- Each level tests your understanding of subnetting and routing
- Export configurations for each completed level

### Submission Requirements

1. **Export all 10 configuration files** (one per level)
2. **Place exported files at the repository root**
3. File format: `.json`
4. Submission structure:
   ```
   net-practice/
   ├── README.md
   ├── config_level_1.json
   ├── config_level_2.json
   ├── ...
   └── config_level_10.json
   ```

---

## Resources

### Core Networking Documentation

- [RFC 791 - Internet Protocol](https://tools.ietf.org/html/rfc791) — IPv4 specification
- [RFC 4632 - Classless Inter-domain Routing](https://tools.ietf.org/html/rfc4632) — CIDR notation
- [TCP/IP Model Layers](https://en.wikipedia.org/wiki/Internet_protocol_suite#Layers) — OSI vs TCP/IP comparison
- [Network Chuck](https://youtu.be/5WfiTHiU4x8?si=5YghrnNk1Toq6zxk) — Subnetting Playlist

### Key Concepts

| Concept | Definition |
|---------|-----------|
| **Subnet Mask** | Defines network/host portions of an IP address |
| **IP Address** | Unique label assigned to a device. Identifies host & network location. |
| **Network ID** | First address in a subnet; identifies the subnet's network |
| **Default Gateway** | (Network ID) Router interface for packets destined outside local network |
| **Usable Hosts** | Range of usable hosts: Default Gateway +1 up to Broadcast Address -1 |
| **Broadcast Address** | Last address in subnet; reaches all hosts on network |
| **CIDR Notation** | `e.g. "/24"` notation indicating number of network bits |
  
------
  
## CIDR Prefix Table

A simple illustration of how CIDR prefix changes the number of subnets, block size, subnet mask in binary, and usable hosts.

Usable hosts are calculated with:
```text
2^n - 2
```
Where `n` is the number of host bits remaining. Reserved 2 hosts for both network and broadcast addresses.  
Borrowed Bits = /CIDR - /24
    
| CIDR | Borrowed Bits | n-Subnets | Block Size | Last Octet | Host Bits | Usable Hosts |
|------|------------|------------|------------|------------|------------|---------------------------|
| /24 | /24 - /24 = 0 | 2<sup>0</sup> = 1 | 256 / 1 = 256 | 00000000 | 8 | 2<sup>8</sup>-2 = 254 |
| /25 | /25 - /24 = 1 | 2<sup>1</sup> = 2 | 256 / 2 = 128 | 10000000 | 7 | 2<sup>7</sup>-2 = 126 |
| /26 | /26 - /24 = 2 | 2<sup>2</sup> = 4 | 256 / 4 = 64 | 11000000 | 6 | 2<sup>6</sup>-2 = 62 |
| /27 | /27 - /24 = 3 | 2<sup>3</sup> = 8 | 256 / 8 = 32 | 11100000 | 5 | 2<sup>5</sup>-2 = 30 |
| /28 | /28 - /24 = 4 | 2<sup>4</sup> = 16 | 256 / 16 = 16 | 11110000 | 4 | 2<sup>4</sup>-2 = 14 |
| /29 | /29 - /24 = 5 | 2<sup>5</sup> = 32 | 256 / 32 = 8 | 11111000 | 3 | 2<sup>3</sup>-2 = 6 |
| /30 | /30 - /24 = 6 | 2<sup>6</sup> = 64 | 256 / 64 = 4 | 11111100 | 2 | 2<sup>2</sup>-2 = 2 |

## Subnetting and Bitmasking

Subnetting works by borrowing bits from the host portion of an IP address.
Example:
- A `/24` leaves 8 host bits
- A `/25` borrows 1 host bit for subnetting, leaving 7 host bits
- A `/26` borrows 2 host bits, leaving 6 host bits, and so on  

As more bits are borrowed:
- Number of subnets increases
- Block size becomes smaller
- Number of usable hosts decreases
  
The binary column shows which bits in the last octet belong to the subnet mask:
```text
/24 = 00000000
/25 = 10000000
/26 = 11000000
/27 = 11100000
and so on ..
```
Each additional `1` means one more borrowed bit. That is why subnetting and bitmasking are directly proportional. As the subnet mask determines how many addresses belong to each subnet and how many hosts can exist inside it.
  
---
  
### AI Usage Disclosure

- **README:** AI assisted in formatting sections to meet 42 requirements
- **Clarity:** Use of AI for asking niche questions regarding network concepts

---

### Technical Notes

- This project is **interactive training only** — no compilation required
- Web interface runs locally, no internet connection needed after setup
- Configuration exports validate CIDR math and routing logic automatically
  
---
