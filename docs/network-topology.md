# Network Topology

## Current Physical Topology

```text
Internet
   |
Spectrum Router
   |
TP-Link Managed Switch
   |------------------- Admin / Gaming PC
   |
   +------------------- Dell OptiPlex 5070 Micro
                           |
                        Proxmox VE
                           |
                 +---------+---------+
                 |                   |
               VM(s)               VM(s)
```

This diagram will evolve as VLANs, virtual switches, network services, and additional lab systems are added.

## Planned Logical Topology

Future versions will document:

- VLAN IDs
- Subnets
- Default gateways
- Trunk and access ports
- Virtual bridges
- Server roles
- DNS / DHCP relationships
- Routing paths
