# 03 – Cisco Secure Firewall 3105 Threat Defense Architecture

*Provision an enterprise-grade firewall boundary, engineer strict access matrices, deploy deep packet inspection (DPI), and architect cryptographic SSL decryption.*

---

## Overview

This module encompasses a six-part engineering progression on a physical Cisco Secure Firewall 3105 Threat Defense appliance. The labs transition the hardware through complex routing and filtering scenarios, moving from baseline Access Control logic to advanced Deep Packet Inspection (DPI). The focus encompasses defining precise logical objects within the Firepower Device Manager (FDM), integrating Snort 3 intrusion prevention, and fundamentally addressing DPI constraints via cryptographic Man-in-the-Middle (MitM) SSL decryption.

📄 **Project Walkthroughs:** Each phase is documented in its respective sub-directory with complete execution methodology, FDM configuration notes, and ingress flow packet validation.

---

## Key Highlights

* **Ingress Routing & Policy Specificity:** Diagnosed and bypassed implicit Dynamic PAT drop logic and default deny matrices that overrode overly broad ANY-to-ANY rules by enforcing strict routing intent via custom FDM Network Objects.
* **Layer 7 Application Control & Shadowing:** Primed the Snort engine for DPI, filtering high-bandwidth application signatures (BitTorrent, Netflix) and Talos URL categories while identifying and resolving top-down access matrix shadowing.
* **Snort 3 IPS & Protocol Evasion:** Bound Cisco Talos Intrusion Policies to permissive egress rules, validating the engine's Protocol Preprocessing logic during simulated mismatched protocol-layer exploit injections over RPC.
* **Security Intelligence (SI) Pre-Filtering:** Engineered a manual workaround to bypass air-gapped cloud threat feed constraints, using custom object instantiation to validate absolute early-stage ingress packet drops.
* **Malware Defense & TLS Blind Spots:** Integrated real-time Talos malware defense, documenting fundamental DPI architectural constraints when confronting upstream proxy HTML substitution and end-to-end TLS encryption.
* **Cryptographic MitM & SSL Decryption:** Generated a localized RSA-2048 Certificate Authority, injected endpoint trust into the Windows OS via `certmgr.msc`, and deployed a Decrypt-Resign matrix to successfully tear open and inspect outbound TLS-encrypted payloads.

---

## Contact

For any questions or feedback, reach out:

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio