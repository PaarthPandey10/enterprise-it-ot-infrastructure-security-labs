# 3.3 – Snort 3 Intrusion Prevention System (IPS) Integration & Validation

*Deploy the Cisco Snort 3 engine, bind Talos intelligence to permissive access rules, and validate protocol preprocessing through simulated network attacks.*

---

## Overview

This engineering lab encompasses the deployment and validation of the Cisco Snort 3 Intrusion Prevention System (IPS) on a Secure Firewall 3105 Threat Defense appliance. The primary objective is to enforce deep packet inspection on active transit traffic to defend the internal workstation segment. This module highlights the architectural constraint of binding DPI engines strictly to permissive rules and explores advanced engine behaviors, specifically Protocol Preprocessing logic, during simulated evasion attempts.

📄 **Full Walkthrough:** For the complete narrative report, configuration steps, and evasion log analysis, see the [Infrastructure Build Guide](./3.3-build-guide.md).

---

## Key Highlights

* **Access Control Audit & DPI Constraints:** Confirmed the architectural limitation that IPS policies cannot be assigned to explicit "Block" rules, as the ASIC drops these packets before CPU-intensive deep packet inspection can occur.
* **Snort 3 Policy Assignment:** Bound the strict `Security Over Connectivity` Cisco Talos IPS policy exclusively to the permissive `Inside_Outside_Rule` to inspect allowed egress payloads against 48,000+ threat signatures.
* **Engine Compilation & Deployment:** Compiled the Snort 3 rulesets and pushed the inspection engine to active ASIC hardware memory.
* **Attack Simulation & Evasion Testing:** Executed internal-to-external Nmap scans and mismatched protocol-layer exploit injections (routing a directory traversal exploit via HTTP over TCP Port 135).
* **Logging & Protocol Preprocessing Validation:** Verified the engine's application-aware constraints. The Snort engine bypassed the exploit signatures due to a protocol-to-port mismatch, successfully logging the allowed connections in the Event Viewer while demonstrating active Protocol Preprocessing behavior.

---

## Technical Specifications

* **Core Routing Engine:** Cisco Secure Firewall 3105 Threat Defense | Routed Mode
* **Firmware:** Version 7.3.1 (Build 19)
* **Inspection Engine:** Snort 3 (3.1.36.100-2)
* **Intrusion Policy:** Security Over Connectivity (Cisco Talos)
* **Simulated Attack Vectors:** Nmap (-A -T4), HTTP directory traversal via TCP 135 (RPC)

---

## Contact

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio