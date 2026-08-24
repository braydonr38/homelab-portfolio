# IP Address Plan

> Update this document whenever an address, subnet, reservation, VLAN, or gateway changes.

## Existing Home LAN

| Device | Address | Assignment | Notes |
|---|---|---|---|
| Router / Default Gateway | TBD | Router | Main LAN gateway |
| Proxmox Server | TBD | DHCP reservation / static management address | Hypervisor management |
| Admin PC | TBD | DHCP | Main management workstation |

## Future Lab Networks

| Network | VLAN | Purpose | Gateway |
|---|---:|---|---|
| Management | TBD | Infrastructure management | TBD |
| Servers | TBD | Server VMs | TBD |
| Clients | TBD | Test endpoints | TBD |
| Guest / Isolated | TBD | Isolation and ACL testing | TBD |

## Documentation Rules

- Never publish public IP addresses, passwords, API keys, Wi-Fi passwords, or private credentials.
- Private RFC1918 IP addresses may be documented when useful.
- Update diagrams and project documentation after major topology changes.
