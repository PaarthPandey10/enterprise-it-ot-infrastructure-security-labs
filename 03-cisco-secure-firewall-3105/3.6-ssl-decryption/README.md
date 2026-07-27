# Project 3.6 – Cryptographic Man-in-the-Middle (MitM) & SSL Decryption

*Generate an internal Certificate Authority, inject OS-level cryptographic trust, and deploy a Decrypt-Resign architecture to inspect TLS-encrypted payloads.*

---

## Overview

This engineering lab directly addresses the Deep Packet Inspection (DPI) constraints identified in previous modules by engineering a cryptographic Man-in-the-Middle (MitM) architecture on a Cisco Secure Firewall 3105. The objective is to deploy a localized Certificate Authority, securely inject endpoint trust into the Windows OS, and configure a "Decrypt-Resign" policy matrix. This enables the hardware routing engine to dynamically spoof external web certificates, tear open outbound TLS tunnels, and expose previously hidden payloads to the underlying File Control and IPS engines.

📄 **Full Walkthrough:** For the complete narrative report, cryptographic configuration steps, and OS integration, see the [Infrastructure Build Guide](./3.6-build-guide.md).

---

## Key Highlights

* **Internal CA Generation:** Engineered a Self-Signed Internal Certificate Authority (`firepower-ssl-ca`) utilizing an RSA-2048 bit keypair directly on the FTD appliance.
* **OS Trust Injection:** Extracted the public `.crt` certificate and seamlessly injected it into the Dell Precision endpoint’s Windows OS via the `certmgr.msc` MMC snap-in, explicitly binding it to the Trusted Root Certification Authorities store.
* **Decrypt-Resign Deployment:** Configured an active SSL Decryption rule (`MitM-Outbound-Intercept`) forcing the hardware to dynamically spoof outbound HTTPS traffic and expose payloads for deep packet inspection.
* **Environmental Routing Audit:** Documented client-side routing behaviors and lab gateway bypass mechanisms to account for air-gapped constraints while maintaining a fully staged internal closed-loop inspection infrastructure.

---

## Technical Specifications

* **Core Routing Engine:** Cisco Secure Firewall 3105 Threat Defense | Routed Mode
* **Firmware:** Version 7.3.1 (Build 19)
* **Cryptographic Architecture:** RSA-2048 Internal CA
* **Action Type:** SSL Decryption (Decrypt - Resign)
* **Endpoint Integration:** Windows Trusted Root Certification Authorities (`certmgr.msc`)

---

## Contact

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio