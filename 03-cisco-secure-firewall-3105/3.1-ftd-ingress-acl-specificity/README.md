# Project 3.1 – FTD Ingress Routing & Access Control Specificity

*Troubleshoot ambiguous drop logic, define explicit network objects, and validate targeted security policy injection on a Cisco Secure Firewall 3105.*

---

## Overview

This engineering lab covers the end-to-end autopsy of an ingress routing failure caused by broad ANY-to-ANY access control rules. The objective focuses on diagnosing the packet drops, instantiating precise logical network objects within the Firepower Device Manager (FDM), and pushing an explicit policy override to the hardware ASIC to confidently permit un-NAT'd ingress ICMP traffic.

📄 **Full Walkthrough:** For the complete narrative report, configuration steps, and flow validation, see the [Infrastructure Build Guide](./3.1.6-build-guide.md).

---

## Key Highlights

* **Policy Ambiguity Identification:** Identified FTD hardware dropping packets despite permissive ANY-to-ANY rules, caused by implicit deny matrices and Dynamic PAT overrides lacking strict routing intent.
* **Logical Object Creation:** Defined a custom Network Object (`inside_subnet`) rigidly mapped to the `192.168.95.0/24` CIDR block representing the internal boundary.
* **Explicit Policy Injection:** Replaced broad destination parameters with the explicit `inside_subnet` object across the `outside_zone` and `inside_zone`.
* **Hardware-Level Validation:** Compiled the changes, pushed to the FTD ASIC, and successfully executed ICMP flow validation from the untrusted node (`192.168.20.100`) to the internal boundary (`192.168.95.100`).

---

## Technical Specifications

* **Core Routing Engine:** Cisco Secure Firewall 3105 Threat Defense | Routed Mode
* **Firmware:** Version 7.3.1 (Build 19)
* **Untrusted Node (Source):** `192.168.20.100` (outside_zone)
* **Internal Boundary (Destination):** `192.168.95.100` (inside_zone / `192.168.95.0/24`)

---

## Contact

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio
