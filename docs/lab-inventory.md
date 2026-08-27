# Lab Inventory

> Physical hardware and major systems used in the homelab. Network addressing and topology are documented separately.

## Server PC

| Component       | Details                                   |
| --------------- | ----------------------------------------- |
| Model           | Dell OptiPlex 5070 Micro                  |
| CPU             | Intel Core i5-9500T, 6 cores / 6 threads  |
| RAM             | 24 GB DDR4                                |
| Primary Storage | 256 GB M.2 PCIe SSD                       |
| Hypervisor      | Proxmox VE 9.2.2                          |
| Virtualization  | Intel VT-x and VT-d enabled               |
| Network         | Integrated Ethernet NIC                   |
| Role            | Hypervisor and virtual server host        |

## Networking Equipment

| Device            | Model / Type             | Purpose                                                      |
| ----------------- | ------------------------ | ------------------------------------------------------------ |
| Router            | Spectrum Router          | Internet gateway and existing home network                   |
| Managed Switch    | TP-Link TL-SG108E        | Managed Layer 2 switching, VLAN labs, and switching practice |
| Admin Workstation | Windows 11 Desktop       | Lab administration and testing endpoint                      |
| Server            | Dell OptiPlex 5070 Micro | Proxmox hypervisor and virtual server host                   |

## Current Software Platform

| Platform           | Purpose                                                         |
| ------------------ | --------------------------------------------------------------- |
| Proxmox VE 9.2.2   | Hypervisor and centralized virtual machine/container management |
| Ubuntu Server 24.04.4 LTS | Linux server operating system running as VM 100           |

## Active Virtual Systems

### `ubuntu-srv01`

| Component        | Details                                      |
| ---------------- | -------------------------------------------- |
| Proxmox VM ID    | 100                                          |
| Operating System | Ubuntu Server 24.04.4 LTS                    |
| vCPUs            | 2                                            |
| Memory           | 4 GB                                         |
| Virtual Disk     | 24 GB                                        |
| Virtual NIC      | VirtIO                                       |
| Network Bridge   | `vmbr0`                                      |
| Guest Interface  | `ens18`                                      |
| Addressing       | DHCP                                         |
| QEMU Guest Agent | Installed and running                        |
| OpenSSH Server   | Installed                                    |
| Role             | General-purpose Linux administration VM      |

`ubuntu-srv01` is the first deployed virtual server in the homelab and will be used for Linux administration practice and future network-service projects.

## Planned Virtual Systems and Services

Planned systems and services may include:

* DNS / Pi-hole server
* DHCP lab server
* Web server
* Monitoring server
* Additional client systems for network testing

Systems will be added to the active inventory as they are deployed.

## Related Documentation

* `ip-address-plan.md` — IP addresses, subnets, gateways, and future VLAN addressing
* `network-topology.md` — physical and logical network connections
* `ccna-skills-matrix.md` — networking objectives practiced throughout the lab
* `../projects/02-proxmox-virtualization/` — Proxmox and Ubuntu VM deployment evidence
* Project documentation — configurations, testing procedures, screenshots, and results
