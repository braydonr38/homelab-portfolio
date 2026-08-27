# IP Address Plan

> Update this document whenever an address, subnet, reservation, VLAN, or gateway changes.

## Existing Home LAN

**Network:** `192.168.1.0/24`  
**Subnet Mask:** `255.255.255.0`  
**Default Gateway:** `192.168.1.1`

| Device            | IP Address     | Address Assignment       | Notes                                                                                       |
| ----------------- | -------------- | ------------------------ | ------------------------------------------------------------------------------------------- |
| Spectrum Router   | `192.168.1.1`  | Router / Default Gateway | Main LAN gateway and current DNS resolver                                                   |
| Proxmox Server    | `192.168.1.53` | DHCP reservation         | Dell OptiPlex 5070 Micro; Proxmox management interface on `vmbr0`                           |
| Ubuntu Server VM  | `192.168.1.10` | DHCP                     | `ubuntu-srv01`; VM 100 hosted on Proxmox and connected to the LAN through `vmbr0`           |
| TP-Link TL-SG108E | `192.168.1.9`  | Management address       | Managed switch web interface                                                                |
| Admin PC          | DHCP           | DHCP                     | Primary management workstation                                                              |

## Physical Network Notes

* Proxmox server is connected to **Port 5** of the TP-Link TL-SG108E.
* Proxmox server link negotiates at **1 Gbps**.
* Proxmox management traffic uses the `vmbr0` Linux bridge.
* The Proxmox physical Ethernet interface `nic0` is attached to `vmbr0`.
* `ubuntu-srv01` uses a VirtIO virtual NIC connected to `vmbr0`, allowing the VM to access the physical LAN through the Proxmox host.
* The current home LAN uses the `192.168.1.0/24` subnet.
* Traffic destined outside the local subnet is forwarded to the default gateway at `192.168.1.1`.

## Future Lab Networks

These networks are planned and will be assigned addressing as VLANs and network segmentation are implemented.

| Network          | VLAN | Purpose                   | Gateway |
| ---------------- | ---- | ------------------------- | ------- |
| Management       | TBD  | Infrastructure management | TBD     |
| Servers          | TBD  | Server VMs and services   | TBD     |
| Clients          | TBD  | Test endpoints            | TBD     |
| Guest / Isolated | TBD  | Isolation and ACL testing | TBD     |

## Documentation Rules

* Never publish public IP addresses, passwords, API keys, Wi-Fi passwords, private keys, or other private credentials.
* Private RFC1918 IP addresses may be documented when useful.
* Document management addresses and DHCP reservations used by lab infrastructure.
* Update this document whenever an infrastructure IP address, subnet, VLAN, reservation, or gateway changes.
* Update network diagrams and related project documentation after major topology changes.
* Verify addressing information from the actual devices before documenting it.
