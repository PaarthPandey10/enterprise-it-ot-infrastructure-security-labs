# OT Security & ICS Network Defense Labs

Hands-on Operational Technology (OT) and Enterprise IT assignments — configuring enterprise-grade industrial firewalls, multilayer switches, and bare-metal infrastructure.

## Table of Contents

* [About](#about)
* [Usage / How to Use](#usage--how-to-use)
* [Features / Highlights](#features--highlights)
* [Technologies Used](#technologies-used)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

---

## About

This repository contains real-world hardware and network security assignments completed while working with physical enterprise infrastructure.

Each lab explores the configuration, segmentation, and defense of network boundaries using equipment from Siemens, Cisco, Fortinet, and Advantech. The focus is on bridging the gap between theoretical network design and the harsh realities of physical silicon deployment.

---

## Project Structure

```
ot-security-and-ics-network-labs/
├── screenshots/
├── 01-siemens-scalance-firewall/
│   ├──  01-build-guide.md
│   └── README.md
├── 02-cisco-sf300-l3-multilayer-architecture/
│   ├──  02-build-guide.md
│   └── README.md
└── LICENSE
```

---

## Usage / How to Use

Each folder contains a lab with:

* Summary of the objective
* Key concepts or OT services used
* PowerShell scripts, architecture logic, or configuration notes

> **Note:** All visual documentation, topology diagrams, and command-line outputs are stored in the centralized `screenshots/` directory.

Start from **Lab 01** to follow the progression from basic industrial boundary setup, moving to **Lab 02** for core multilayer switching and control plane debugging.

---

## Features / Highlights

* Provisioned bare-metal firewall and switch hardware.
* Bypassed legacy cryptography deprecation using OpenSSH override flags.
* Diagnosed hardware control plane exhaustion and established Out-of-Band (OOB) serial management.
* Configured Industrial and Enterprise Port-Based VLANs.
* Routed and secured protocols across ASIC hardware backplanes.
* Engineered local "Living off the Land" SOC telemetry pipelines using Syslog and native PowerShell.

---

## Technologies Used

* **Hardware:** Siemens SCALANCE SC646-2C, Cisco Secure Firewall 3100, Cisco SF300-24P Switch, Weidmüller PROeco Power Supply
* **Software & Tools:** Siemens PRONETA, Windows PowerShell, PuTTY (Serial/OOB)
* **Protocols/Concepts:** Modbus TCP, S7, ICMP, Syslog, IPv4, Inter-VLAN Routing, SVI Autostate, OpenSSH Cryptography

---

## Contributing

Not open for contributions — personal practice lab and hardware portfolio showcase.

---

## License

This project is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).

**You are free to:**

* **Share** — copy and redistribute the material in any medium or format
* **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

**Under the following terms:**

* **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

🔗 [View License](https://creativecommons.org/licenses/by/4.0/)

---

## Contact

**Paarth Pandey**
[LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com) | paarthdxb@gmail.com

---

*Note: All labs in this repository are based on hands-on engineering work with physical Operational Technology (OT) and IT hardware. Screenshots and command flows are reused respectfully for learning and documentation purposes only.*

---
> Author: Paarth Pandey
>
> OT Security Labs: Industrial Network Defense


