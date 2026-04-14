# Proxmox VM Inventory

## Apricot (192.168.1.201)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 108 | Puppetdb | running | 4 | 8GB | 45G | 192.168.1.247 | ssh puppetdb@192.168.1.247 |

## Butternut (192.168.1.202)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 106 | Puppet | running | 4 | 8GB | 64G | 192.168.1.246 | ssh puppet-homelab@192.168.1.246 |

## Cupcake (192.168.1.203)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 112 | HAOS | running | 8 | 16GB | 32G | 192.168.1.130 | N/A (UI only) |

## Dessert (192.168.1.204)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 105 | Windows-VM | stopped | 6 | 24GB | 120G | DHCP | N/A (template) |
| 110 | CLI-Docker | running | 8 | 8GB | 64G | 192.168.1.80 | ssh ubuntu@192.168.1.80 |

## Echo (192.168.1.205)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 100 | Ubuntu-ServerCLI-Template | stopped | 6 | 16GB | 64G | DHCP | N/A (template) |
| 101 | Plex | running | 16 | 64GB | 64G | 192.168.1.155 | ssh bcsb@192.168.1.155 |
| 102 | Ubuntu-Desktop-Template | stopped | 8 | 16GB | 64G | DHCP | N/A (template) |
| 103 | Kali | stopped | 4 | 6GB | 80G | 192.168.1.238 | ssh bcsb@192.168.1.238 |
| 104 | Super-Admin | stopped | 16 | 60GB | 64G | 192.168.1.131 | ssh ubuntu@192.168.1.131 |
| 107 | Qbit | running | 8 | 32GB | 64G | 192.168.1.147 | ssh bcsb@192.168.1.147 |

## Node NIC Notes
- Dessert eno2: TX ring buffer set to 4096, flow control disabled (Intel e1000e)
- Echo enp42s0: Flow control disabled (Realtek r8169, capped at 256 TX rings — Intel I350 PCIe upgrade recommended)
