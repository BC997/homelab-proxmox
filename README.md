# homelab-proxmox

Proxmox 5-node cluster configuration, VM inventory, and NIC tuning documentation for a self-hosted homelab. Includes network interface configs, post-cluster-outage NIC fixes, and a full VM inventory across all nodes.

## Cluster Overview

5-node Proxmox 8.4.0 cluster running on Debian. All nodes share a common bridge (vmbr0) and are managed via the Proxmox web UI and CLI.

## Node Summary

| Node | Role |
|------|------|
| Apricot | PuppetDB host |
| Butternut | Puppet primary host |
| Cupcake | Home Assistant OS host |
| Dessert | Docker infrastructure host |
| Echo | Media server and admin workstation |

## NIC Tuning

Two nodes required post-deployment NIC fixes to resolve a TX queue hang that caused a full cluster outage via Corosync quorum loss:

- **Dessert** — Intel e1000e: TX ring buffer increased to 4096, flow control disabled
- **Echo** — Realtek r8169: Flow control disabled (hardware capped at 256 TX rings)

Fixes are applied persistently via post-up directives in `/etc/network/interfaces`.

## Repository Structure

    proxmox-repo/
    ├── nodes/
    │   ├── apricot/interfaces
    │   ├── butternut/interfaces
    │   ├── cupcake/interfaces
    │   ├── dessert/interfaces
    │   └── echo/interfaces
    └── vm-inventory/
        └── inventory.md

## Stack
- Proxmox VE 8.4.0
- Debian 12
- Corosync cluster networking
- Open Source Puppet 8 for VM configuration management
