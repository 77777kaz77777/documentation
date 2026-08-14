Since you are building a comprehensive Google Doc, this Proxmox VE (Virtual Environment) cheatsheet is divided into the two main command sets: qm for Virtual Machines (QEMU/KVM) and pct for Containers (LXC)[cite: 22].
## **🖥️ Proxmox Virtual Machine Commands (qm)**
These commands manage full virtual machines. Replace [vmid] with the numerical ID of your VM (e.g., 100)[cite: 22].
|  |  |
| :- | :- |
| Action | Command |
| **List All VMs** | qm list[cite: 22] |
| **Start VM** | qm start [vmid][cite: 22] |
| **Stop VM (Graceful)** | qm shutdown [vmid][cite: 22] |
| **Stop VM (Immediate)** | qm stop [vmid][cite: 22] |
| **Reset VM** | qm reset [vmid][cite: 22] |
| **Clone VM** | qm clone [vmid] [newid] --name [name][cite: 22] |
| **Remove VM** | qm destroy [vmid][cite: 22] |
| **Unlock VM** | qm unlock [vmid] (Used if a task hangs)[cite: 22] |
| **Show Config** | qm config [vmid][cite: 22] |
| **Terminal Proxy** | qm terminal [vmid][cite: 22] |

## **📦 Proxmox Container Commands (pct)**
These are specific to the LXC containers running on your Proxmox host[cite: 22].
|  |  |
| :- | :- |
| Action | Command |
| **List All Containers** | pct list[cite: 22] |
| **Start Container** | pct start [vmid][cite: 22] |
| **Stop Container** | pct stop [vmid][cite: 22] |
| **Enter Shell** | pct enter [vmid][cite: 22] |
| **Execute Command** | pct exec [vmid] -- [command][cite: 22] |
| **Show Config** | pct config [vmid][cite: 22] |
| **Clone Container** | pct clone [vmid] [newid] --hostname [name][cite: 22] |
| **Mount CT Disk** | pct mount [vmid][cite: 22] |
| **Unmount CT Disk** | pct unmount [vmid][cite: 22] |

## **💾 Storage & Backup (vzdump/pvesm)**
Proxmox uses vzdump for backups and pvesm for storage management[cite: 22].
|  |  |
| :- | :- |
| Action | Command |
| **Backup VM/CT** | vzdump [vmid] --storage [storage_name] --compress lzo[cite: 22] |
| **Restore VM** | qmrestore [backup_file] [vmid][cite: 22] |
| **Restore Container** | pct restore [vmid] [backup_file][cite: 22] |
| **List Storage Pools** | pvesm status[cite: 22] |
| **List Content in Pool** | pvesm list [storage_name][cite: 22] |
| **Free Up Space** | pvesm free [storage_name]:[volume][cite: 22] |

## **🌐 Cluster & System Management**
Use these for node-level operations and health checks[cite: 22].
|  |  |
| :- | :- |
| Action | Command |
| **Cluster Status** | pvecm status[cite: 22] |
| **Check Services** | systemctl status pve-cluster[cite: 22] |
| **Update Node Repos** | apt update[cite: 22] |
| **Update Proxmox** | apt dist-upgrade[cite: 22] |
| **View Task Logs** | cat /var/log/pve/tasks/index[cite: 22] |
| **Restart Web GUI** | systemctl restart pveproxy[cite: 22] |

## **⚠️ Common Troubleshooting**
  - **Fix "No Subscription" Error:** If you are using the free version, you often need to disable the enterprise repo in /etc/apt/sources.list.d/pve-enterprise.list[cite: 22].
  - **Zombie Locks:** If a VM is stuck in a "locked" state after a failed backup, use qm unlock [vmid][cite: 22].
  - **High CPU/Load:** Use htop (you may need to install it with apt install htop) to see which process is eating resources on the host[cite: 22].
Would you like me to include the **Port Reference** I mentioned earlier (listing the default ports for Proxmox, SSH, Web GUIs, etc.)?[cite: 22]
