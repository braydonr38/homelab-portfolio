# Network Topology

> Documents the physical and logical relationships between homelab devices. IP addressing and detailed hardware information are maintained in their respective documentation files.

## Current Physical Topology

```text id="p4p57f"
Internet
   |
Spectrum Router
   |
   +------------------- TP-Link TL-SG108E
                           |
                           +--- Port 5 (1 Gbps)
                                   |
                                   +--- Dell OptiPlex 5070 Micro
                                            |
                                         Proxmox VE
```

The Proxmox server's connection to Port 5 was verified through physical link-state testing during Project 04.

Other home-network devices are intentionally omitted from this diagram unless they become relevant to a homelab project.

## Current Logical Topology

```text id="sgbuj2"
Existing Home LAN
       |
Spectrum Router
       |
TP-Link TL-SG108E
       |
   Proxmox Host
       |
     vmbr0
       |
     nic0
       |
Physical Ethernet
```

Proxmox currently uses the `vmbr0` Linux bridge for its management network connection. The physical Ethernet interface `nic0` is attached to this bridge.

Virtual machines and containers will be added to the logical topology only after they are deployed.

## Planned Topology Development

As the homelab expands, future versions of this document will incorporate:

* Virtual machines and containers
* VLAN boundaries
* Tagged and untagged switch links
* Access and trunk port roles
* Additional Proxmox bridges where required
* Inter-VLAN routing paths
* DNS and DHCP service relationships
* Pi-hole DNS filtering
* Monitoring and logging infrastructure
* Network segmentation and security controls

## Related Documentation

* `lab-inventory.md` — physical hardware and major systems
* `ip-address-plan.md` — IP addresses, subnets, gateways, and VLAN addressing
* `ccna-skills-matrix.md` — hands-on networking skills and project evidence
* `../projects/04-managed-switch/` — managed switch configuration and link-state troubleshooting evidence
