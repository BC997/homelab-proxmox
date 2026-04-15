# Proxmox VM Inventory

## Apricot (10.0.0.201)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 108 | Puppetdb | running | 4 | 8GB | 45G | 10.0.0.247 | N/A |

## Butternut (10.0.0.202)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 106 | Puppet | running | 4 | 8GB | 64G | 10.0.0.246 | N/A |

## Cupcake (10.0.0.203)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 112 | HAOS | running | 8 | 16GB | 32G | 10.0.0.130 | N/A (UI only) |

## Dessert (10.0.0.204)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 105 | Windows-VM | stopped | 6 | 24GB | 120G | DHCP | N/A (template) |
| 110 | CLI-Docker | running | 8 | 8GB | 64G | 10.0.0.80 | N/A |

## Echo (10.0.0.205)
| VMID | Name | Status | CPUs | RAM | Disk | IP | SSH |
|------|------|--------|------|-----|------|----|-----|
| 100 | Ubuntu-ServerCLI-Template | stopped | 6 | 16GB | 64G | DHCP | N/A (template) |
| 101 | Plex | running | 16 | 64GB | 64G | 10.0.0.155 | N/A |
| 102 | Ubuntu-Desktop-Template | stopped | 8 | 16GB | 64G | DHCP | N/A (template) |
| 103 | Security-VM | stopped | 4 | 6GB | 80G | 10.0.0.238 | N/A |
| 104 | Super-Admin | stopped | 16 | 60GB | 64G | 10.0.0.131 | N/A |

## Node NIC Notes
- Dessert eno2: TX ring buffer set to 4096, flow control disabled (Intel e1000e)
- Echo enp42s0: Flow control disabled (Realtek r8169, capped at 256 TX rings — Intel I350 PCIe upgrade recommended)
