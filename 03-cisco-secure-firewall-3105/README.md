# 03 – Cisco Secure Firewall 3105 Threat Defense Architecture

*Provision an enterprise-grade firewall boundary, debug ingress traffic flows, and engineer strict access control matrices using explicit network object instantiation.*

---

## Overview

This module encompasses the configuration, troubleshooting, and deployment of a physical Cisco Secure Firewall 3105 Threat Defense (FTD) appliance. The labs transition the hardware through complex routing scenarios, focusing heavily on bypassing ambiguous drop logic, defining precise logical objects within the Firepower Device Manager (FDM), and enforcing strict hardware-level routing intent. 

📄 **Project Walkthroughs:** Each phase is documented in its respective sub-directory with complete execution methodology, FDM configuration notes, and ingress flow packet validation.

---

## Key Highlights

* **Ingress Routing & Access Control Specificity:** Diagnosed and bypassed implicit Dynamic PAT drop logic and default deny matrices that overrode overly broad ANY-to-ANY permissive rules.
* **Network Object Instantiation:** Mapped physical subnets to rigid logical Network Objects within the FDM database to enforce strict destination parameters for the ASIC routing engine.
* **Explicit Policy Override:** Injected targeted Security Policies across defined physical zones (outside_zone to inside_zone) to successfully permit un-NAT'd ingress traffic across the hardware backplane.
* **Hardware Deployment & Validation:** Pushed compiled web UI configurations directly to the FTD routing engine and validated true hardware bypass using ICMP tracking across isolated broadcast domains.

---

## Contact

For any questions or feedback, reach out:

**Paarth Pandey** | [LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

> Author: Paarth Pandey
> 
> Enterprise IT/OT Infrastructure Security Lab Portfolio
