# 3.2 – Layer 7 Application Control & URL Categorization Engine

*Enable subscription licensing, prime the Snort engine for Deep Packet Inspection (DPI), and engineer granular Layer 7 payload drops while troubleshooting top-down access matrix logic.*

---

## Overview

This engineering lab covers the implementation of Layer 7 application control and URL categorization on a Cisco Secure Firewall 3105 Threat Defense appliance. The objective focuses on moving beyond standard Layer 3/4 filtering to intercept specific high-bandwidth applications and block known malicious URL categories using Cisco's Talos intelligence. It also encompasses the critical diagnosis of access rule "shadowing" conflicts within the Firepower Device Manager (FDM).

📄 **Full Walkthrough:** For the complete narrative report, configuration steps, and logic troubleshooting, see the [Infrastructure Build Guide](./3.2-build-guide.md).

---

## Key Highlights

* **Engine Licensing Validation:** Validated the Smart License portal to ensure URL Filtering, Malware Defense, and Intrusion Prevention System (IPS) engines were active, priming the firewall for DPI.
* **Layer 7 Rule Construction:** Instantiated a targeted drop policy (`block-bad-traffic`) to intercept internal traffic destined for the external zone.
* **Application Signature Filtering:** Bound explicit application definitions to the block condition, successfully isolating BitTorrent, Facebook, and Netflix payloads.
* **Talos URL Categorization:** Applied categorical reputation blocks to 'Games' and 'Social Networking' web traffic to halt related DNS and HTTP/S requests.
* **Policy Matrix Analysis & Remediation:** Identified and resolved a critical 'Shadowing' error where the restrictive block policy was initially placed below a permissive catch-all rule, rendering the block inert due to top-down processing logic.

---

## Technical Specifications

* **Core Routing Engine:** Cisco Secure Firewall 3105 Threat Defense | Routed Mode
* **Firmware:** Version 7.3.1 (Build 19)
* **Source Matrix:** `inside_zone` (Internal boundary)
* **Destination Matrix:** `outside_zone` (Untrusted boundary)
* **Action Types:** Layer 7 Block (Application/URL)

---

## Contact

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio