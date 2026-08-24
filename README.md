# Homelab Portfolio

A hands-on networking and systems administration lab built to develop practical skills, reinforce CCNA objectives, and create employer-ready evidence of configuration, troubleshooting, documentation, and problem solving.

## Lab Goals

* Build practical networking and systems administration experience.
* Practice CCNA concepts in a real environment where possible.
* Learn virtualization, Linux administration, switching, routing, DNS, DHCP, VLANs, monitoring, and troubleshooting.
* Document not only successful configurations, but also problems encountered and how they were resolved.
* Create evidence that can be discussed in technical job interviews.

## Current Lab Hardware

### Server

* Dell OptiPlex 5070 Micro
* Intel Core i5-9500T
* 24 GB DDR4 RAM
* 256 GB M.2 PCIe SSD
* Integrated Ethernet NIC
* Intel VT-x / VT-d virtualization support
* Proxmox VE

### Networking

* Spectrum router
* TP-Link TL-SG108E 8-port managed switch
* Ethernet-connected administration workstation and lab devices

Detailed hardware information is maintained in [`docs/lab-inventory.md`](docs/lab-inventory.md).

## Portfolio Roadmap

| Project                           | Area                        | Status      |
| --------------------------------- | --------------------------- | ----------- |
| 01 - Physical Homelab Build       | Hardware / LAN              | In Progress |
| 02 - Proxmox Virtualization       | Virtualization / Linux      | In Progress |
| 03 - Linux Server Administration  | Systems Administration      | Planned     |
| 04 - Managed Switch Configuration | Switching / Troubleshooting | In Progress |
| 05 - VLAN Lab                     | VLANs / 802.1Q              | Planned     |
| 06 - Inter-VLAN Routing Lab       | Routing                     | Planned     |
| 07 - DHCP and DNS Services        | Network Services            | Planned     |
| 08 - Pi-hole DNS Filtering        | DNS / Linux                 | Planned     |
| 09 - Static Routing Lab           | Routing                     | Planned     |
| 10 - Network Troubleshooting Lab  | Troubleshooting             | Planned     |
| 11 - Monitoring and Logging       | Operations                  | Planned     |
| 12 - Security and Hardening       | Security                    | Planned     |
| 13 - Backup and Recovery          | Systems Administration      | Planned     |
| 14 - Packet Tracer CCNA Labs      | Cisco / CCNA                | Ongoing     |

## What Each Project Documents

Each project is designed to document:

1. **Objective** — what I wanted to build or learn.
2. **Concepts** — networking or systems concepts involved.
3. **Topology** — how relevant devices and networks connect.
4. **Implementation** — configuration steps and commands.
5. **Verification** — how I proved the configuration worked.
6. **Troubleshooting** — problems encountered, symptoms, cause, and resolution.
7. **What I Learned** — explanation of the concepts demonstrated.
8. **Evidence** — screenshots, command output, diagrams, and configuration snippets.
9. **Interview Talking Points** — concise explanations that can be discussed with employers.

## Skills Demonstrated

Hands-on work currently documented in this repository includes:

* IPv4 addressing and subnet verification
* Default gateway and routing-table verification
* Ethernet and Layer 2 networking concepts
* ARP and MAC address resolution
* ICMP connectivity testing
* DNS connectivity testing
* Managed switch administration
* Physical switch-port and link-state troubleshooting
* Ethernet link-speed verification
* Proxmox networking and Linux bridge inspection
* Basic network-device security hardening
* Structured network troubleshooting
* Technical documentation and change verification

Additional networking and systems administration skills will be added as they are practiced and documented throughout the project roadmap.

See [`docs/ccna-skills-matrix.md`](docs/ccna-skills-matrix.md) for detailed skills tracking.

## CCNA Alignment

This lab is intentionally designed to reinforce topics from Cisco's CCNA exam blueprint. Physical equipment, virtual machines, and Cisco Packet Tracer will be used together when a topic cannot reasonably be reproduced in the physical lab.

Skills are marked as practiced only after hands-on configuration, verification, or troubleshooting has been completed.

See [`docs/ccna-skills-matrix.md`](docs/ccna-skills-matrix.md).

## Network Documentation

Central documentation is maintained separately to avoid unnecessarily duplicating information across project files:

* [`docs/lab-inventory.md`](docs/lab-inventory.md) — physical hardware and major systems
* [`docs/ip-address-plan.md`](docs/ip-address-plan.md) — IP addressing, subnets, gateways, and future VLAN addressing
* [`docs/network-topology.md`](docs/network-topology.md) — physical and logical network relationships
* [`docs/ccna-skills-matrix.md`](docs/ccna-skills-matrix.md) — hands-on CCNA skills and project evidence

Detailed configurations, testing procedures, troubleshooting notes, and screenshots are maintained within the relevant project folders.

## Why This Repository Exists

My goal is not simply to say that I have used networking technologies. This repository is intended to demonstrate how I configure systems, verify results, troubleshoot failures, explain technical concepts, and document my work.

As the homelab develops, each project will provide evidence of practical networking and systems administration experience that can be discussed during technical interviews.
