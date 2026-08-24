# Lab Inventory

> Physical hardware and major systems used in the homelab. Network addressing and topology are documented separately.

## Server PC

| Component       | Details                                  |
| --------------- | ---------------------------------------- |
| Model           | Dell OptiPlex 5070 Micro                 |
| CPU             | Intel Core i5-9500T, 6 cores / 6 threads |
| RAM             | 24 GB DDR4                               |
| Primary Storage | 256 GB M.2 PCIe SSD                      |
| Hypervisor      | Proxmox VE                               |
| Virtualization  | Intel VT-x and VT-d enabled              |
| Network         | Integrated Ethernet NIC                  |
| Role            | Hypervisor and virtual server host       |

## Networking Equipment

| Device            | Model / Type              | Purpose                                                      |
| ----------------- | ------------------------- | ------------------------------------------------------------ |
| Router            | Spectrum Router           | Internet gateway and existing home network                   |
| Managed Switch    | TP-Link TL-SG108E         | Managed Layer 2 switching, VLAN labs, and switching practice |
| Admin Workstation | Windows 11 Desktop        | Lab administration and testing endpoint                      |
| Server            | Dell OptiPlex 5070 Micro  | Proxmox hypervisor and virtual server host                   |

## Current Software Platform

| Platform   | Purpose                                                         |
| ---------- | --------------------------------------------------------------- |
| Proxmox VE | Hypervisor and centralized virtual machine/container management |

## Planned Virtual Systems and Services

Planned systems may include:

* Linux administration VM
* DNS / Pi-hole server
* DHCP lab server
* Web server
* Monitoring server
* Additional client systems for network testing

Systems will be added to the active inventory as they are deployed.

## Related Documentation

* `ip-address-plan.md` — IP addresses, subnets, gateways, and future VLAN addressing
* Network topology documentation — physical and logical network connections
* Project documentation — configurations, testing procedures, screenshots, and results
* CCNA skills matrix — networking objectives practiced throughout the lab
