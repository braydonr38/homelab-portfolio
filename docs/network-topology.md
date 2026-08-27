# Network Topology

> Documents the physical and logical relationships between homelab devices. IP addressing and detailed hardware information are maintained in their respective documentation files.

## Current Physical Topology

```text
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

```text
                         Existing Home LAN
                          192.168.1.0/24
                                |
                         Spectrum Router
                          192.168.1.1
                                |
                         TP-Link TL-SG108E
                                |
                         Physical Ethernet
                                |
                              nic0
                                |
                              vmbr0
                           /           \
                          /             \
                         /               \
                Proxmox Host          VM 100
                     pve           ubuntu-srv01
               192.168.1.53        192.168.1.10
                                  VirtIO NIC: ens18
```

The Proxmox host uses the `vmbr0` Linux bridge for its management network connection. The physical Ethernet interface `nic0` is attached to this bridge.

VM 100, `ubuntu-srv01`, is also connected to `vmbr0` through a VirtIO virtual network adapter. Inside Ubuntu, this virtual interface appears as `ens18`.

This allows both the Proxmox host and the Ubuntu VM to communicate on the existing `192.168.1.0/24` LAN while sharing the Dell server's physical Ethernet connection.

The Proxmox host currently uses `192.168.1.53` through a DHCP reservation. The Ubuntu VM currently receives `192.168.1.10` through DHCP.

Traffic destined outside the local `192.168.1.0/24` subnet is forwarded to the Spectrum router at `192.168.1.1`, which serves as the current default gateway.

## Virtual Networking

The current virtual networking path for `ubuntu-srv01` is:

```text
ubuntu-srv01
     |
ens18 (VirtIO virtual NIC)
     |
   vmbr0
     |
   nic0
     |
Dell Physical Ethernet
     |
TP-Link TL-SG108E
     |
Spectrum Router
     |
Home LAN / Internet
```

This configuration allows the virtual machine to operate as an independent network host even though it does not have its own physical Ethernet adapter.

During Project 02, the VM successfully:

* Received an IPv4 address through DHCP
* Communicated with the local default gateway
* Reached an external IPv4 address
* Resolved a domain name through DNS
* Reached an Internet host using IPv4

## Planned Topology Development

As the homelab expands, future versions of this document will incorporate:

* Additional virtual machines and containers
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
* `../projects/02-proxmox-virtualization/` — Proxmox VM deployment and virtual networking evidence
* `../projects/04-managed-switch/` — managed switch configuration and link-state troubleshooting evidence
