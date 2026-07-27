# 3.4 – Security Intelligence (SI) Engine Configuration & Custom Feed Blacklisting

*Deploy the Security Intelligence engine, bypass air-gapped threat feed constraints using custom object instantiation, and validate absolute early-stage ingress drops.*

---

## Overview

This engineering lab focuses on deploying the Security Intelligence (SI) engine on a Cisco Secure Firewall 3105 Threat Defense appliance to serve as a pre-filter drop mechanism. The primary objective is to dynamically vaporize malicious ingress traffic before it even reaches the standard Access Control matrix. This module highlights real-world troubleshooting by engineering a custom workaround to bypass air-gapped network constraints that prevent dynamic Cisco Talos cloud feed updates.

📄 **Full Walkthrough:** For the complete narrative report, configuration steps, and ingress drop validation, see the [Infrastructure Build Guide](./3.4-build-guide.md).

---

## Key Highlights

* **The Air-Gapped Constraint:** Identified and diagnosed limitations within the isolated lab topology that prevented the SI engine from reaching Cisco's cloud servers for dynamic Talos threat feed updates.
* **Custom Object Instantiation:** Engineered a manual SI workaround by creating a custom network object (`simulated-hacker-ip`) mapped explicitly to the untrusted external node (`192.168.20.100`).
* **Pre-Filter Policy Binding:** Injected the custom object directly into the active Security Intelligence Network Block (Drop) list, staging the pre-filter defense matrix.
* **ASIC Deployment & Ingress Drop Validation:** Pushed the SI policy to active hardware memory. Validated efficacy by proving immediate ingress packet drops (100% ICMP loss) and correlating the traffic interception with definitive SI Block actions in the Event Viewer.

---

## Technical Specifications

* **Core Routing Engine:** Cisco Secure Firewall 3105 Threat Defense | Routed Mode
* **Firmware:** Version 7.3.1 (Build 19)
* **Pre-Filter Engine:** Security Intelligence (SI)
* **Simulated Attacker (Source):** `192.168.20.100` (`simulated-hacker-ip`)
* **Internal Target (Destination):** `192.168.95.100`

---

## Contact

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio