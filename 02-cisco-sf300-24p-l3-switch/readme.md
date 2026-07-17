# 02 – Cisco SF300 L3 Multilayer Architecture & Security Fabric

*Provision a legacy multilayer switch, debug control plane exhaustion, and engineer a hardened Layer 3 edge featuring stateless ACLs, anti-spoofing protocols, and secure telemetry.*

---

## Overview

This module encompasses a six-part engineering progression on a physical Cisco SF300-24P switch. The labs transition the hardware from a factory-default state into a highly secure, automated, and monitored Layer 3 edge fabric. The focus extends beyond basic configuration to deep physical debugging—navigating ASIC hardware limitations, legacy cryptographic deprecations, stateless firewall traps, and control plane CPU exhaustion.

📄 **Project Walkthroughs:** Each phase is documented in its respective sub-directory with complete CLI methodology, firmware debugging notes, and wire-speed packet validation.

---

## Key Highlights

* **System Initialization & Cryptographic Bypass:** Bypassed OpenSSH legacy deprecations using forced KEX/Cipher CLI overrides and established Out-of-Band (OOB) serial management to survive severe CPU exhaustion during ASIC routing updates.
* **Stateless Access Control & Zero-Trust:** Deployed unidirectional Layer 3 isolation policies using stateless ACLs, remediating "Default Action" blackhole traps and proving hardware-level packet drops via Hex dump forensics.
* **Infrastructure Automation & Air-Gapping:** Initialized discrete DHCP network pools with static infrastructure exclusions, validating L3 broadcast containment and external internet air-gapping.
* **Anti-Spoofing Hardware Gatekeeper:** Engineered a secure Layer 2/3 boundary using DHCP Snooping, Dynamic ARP Inspection (DAI), and IP Source Guard (IPSG), executing deliberate inverse-spoofing attacks to prove wire-speed ASIC mitigation.
* **RSTP & Self-Healing Topology:** Migrated the core to Rapid Spanning Tree Protocol (802.1w), armed Administrative Edge ports with BPDU Guard to prevent broadcast storms, and automated a 300-second self-healing error recovery loop.
* **Advanced QoS & SNMPv3 Enclaves:** Bypassed Layer 3 TCAM hardware constraints by deploying a CoS/DSCP Trust model. Secured control-plane telemetry by engineering an encrypted, authenticated SNMPv3 (AuthPriv) pipeline using SHA and DES.

---

## Contact

For any questions or feedback, reach out:

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio