# CCNA Skills Matrix

> Tracks hands-on networking skills practiced through the physical homelab, virtual systems, and Cisco Packet Tracer. Detailed procedures, screenshots, and results are maintained in the individual project documentation.

## Skills Tracking

| Skill / Topic                                      | Physical Lab | VM / Server Lab | Packet Tracer | Evidence          | Status      |
| -------------------------------------------------- | ------------ | --------------- | ------------- | ----------------- | ----------- |
| IPv4 addressing                                    | ✓            | ✓               | —             | Projects 02, 04   | In Progress |
| Subnetting                                         | ✓            | ✓               | —             | Projects 02, 04   | In Progress |
| MAC address learning / tables                      | ✓            | ✓               | —             | Project 04        | In Progress |
| ARP                                                | ✓            | ✓               | —             | Project 04        | In Progress |
| Ethernet frames / Layer 2 forwarding               | ✓            | ✓               | —             | Project 04        | In Progress |
| Switch port configuration / verification           | ✓            | —               | —             | Project 04        | In Progress |
| VLANs                                              | —            | —               | —             | —                 | Planned     |
| 802.1Q trunks                                      | —            | —               | —             | —                 | Planned     |
| Inter-VLAN routing                                 | —            | —               | —             | —                 | Planned     |
| Static routing                                     | —            | —               | —             | —                 | Planned     |
| Default routes                                     | ✓            | ✓               | —             | Projects 02, 04   | In Progress |
| DHCP                                               | —            | ✓               | —             | Project 02        | In Progress |
| DNS                                                | ✓            | ✓               | —             | Projects 02, 04   | In Progress |
| ICMP troubleshooting                               | ✓            | ✓               | —             | Projects 02, 04   | In Progress |
| SSH management                                     | —            | —               | —             | —                 | Planned     |
| Network device verification                        | ✓            | ✓               | —             | Projects 02, 04   | In Progress |
| Physical connectivity / link-state troubleshooting | ✓            | ✓               | —             | Project 04        | In Progress |
| Network device hardening                           | ✓            | —               | —             | Project 04        | In Progress |
| ACL concepts                                       | —            | —               | —             | —                 | Planned     |
| NAT concepts                                       | —            | —               | —             | —                 | Planned     |
| Wireless concepts                                  | —            | —               | —             | —                 | Planned     |
| Network monitoring                                 | —            | —               | —             | —                 | Planned     |
| Syslog / logging                                   | —            | —               | —             | —                 | Planned     |

## Status Definitions

* **Planned** — Included in the homelab roadmap but not yet practiced hands-on.
* **In Progress** — Practiced hands-on, but additional configuration or troubleshooting experience is planned.
* **Completed** — Demonstrated multiple times with sufficient hands-on evidence and understanding.
* **Needs Review** — Previously practiced but requires additional review or reinforcement.

## Evidence

Detailed evidence is maintained within the relevant project folders rather than duplicated here.

Current documented evidence:

### Project 02 — Proxmox Virtualization

Hands-on networking and systems administration work included:

* Provisioned an Ubuntu Server virtual machine in Proxmox.
* Connected a VirtIO virtual network interface to the Proxmox `vmbr0` Linux bridge.
* Verified the Ubuntu interface `ens18` received `192.168.1.10/24` through DHCP.
* Used `ip route` to identify and verify the default route through `192.168.1.1`.
* Verified local Layer 3 connectivity by pinging the default gateway.
* Verified external IPv4 connectivity by pinging `1.1.1.1`.
* Verified DNS resolution and IPv4 Internet connectivity using a domain name.
* Troubleshot a domain-name ping that selected IPv6 by default and verified connectivity by explicitly testing IPv4.
* Installed and verified the QEMU Guest Agent to improve communication between the Proxmox host and Ubuntu guest.

### Project 04 — Managed Switch Configuration

Hands-on networking work included:

* IPv4 addressing and subnet verification.
* Routing and default-gateway verification.
* ARP and MAC address investigation.
* Ethernet and Layer 2 forwarding concepts.
* ICMP connectivity testing.
* DNS testing.
* Managed switch administration.
* Switch port and link-state verification.
* Physical connectivity troubleshooting.
* Basic network-device hardening.

Additional project references will be added as skills are practiced throughout the homelab.

## Tracking Approach

A checkmark indicates that the skill has been practiced hands-on in that environment. Planned activities are not marked as completed work.

Skills will be updated as they are configured, verified, and troubleshot throughout the homelab. The goal is to build practical competency across the CCNA curriculum rather than marking a topic complete after a single exercise.

A skill may remain **In Progress** after successful hands-on practice when additional configuration, repetition, troubleshooting, or implementation in another environment is still planned.
