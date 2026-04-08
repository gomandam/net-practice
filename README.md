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
| **Default Gateway** | Router interface for packets destined outside local network |
| **CIDR Notation** | `/24` notation indicating number of network bits |
| **Broadcast Address** | Last address in subnet; reaches all hosts on network |
| **Network Address** | First address in subnet; identifies the network |

### AI Usage Disclosure

- **README structure & formatting:** AI assisted in organizing sections to meet 42 requirements
- **Explanation clarity:** use of AI for asking niche questions regarding network concepts

---

## Technical Notes

- This project is **interactive training only** — no compilation required
- Web interface runs locally, no internet connection needed after setup
- Configuration exports validate CIDR math and routing logic automatically

