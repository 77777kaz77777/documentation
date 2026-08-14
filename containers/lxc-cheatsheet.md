## **📦 LXC/LXD Essentials**
Most modern implementations use the lxc command-line tool (part of the LXD project)[cite: 23].
|  |  |
| :- | :- |
| Action | Command |
| **List Containers** | lxc list[cite: 23] |
| **Launch New Container** | lxc launch images:[distro]/[version] [name][cite: 23] |
| **Example (Ubuntu)** | lxc launch images:ubuntu/24.04 my-ubuntu[cite: 23] |
| **Start Container** | lxc start [name][cite: 23] |
| **Stop Container** | lxc stop [name][cite: 23] |
| **Restart Container** | lxc restart [name][cite: 23] |
| **Delete Container** | lxc delete [name] --force[cite: 23] |
| **Show Container Info** | lxc info [name][cite: 23] |

## **🛠️ Access & Configuration**
Interacting with the "inside" of an LXC container is very similar to interacting with a virtual machine[cite: 23].
|  |  |
| :- | :- |
| Action | Command |
| **Open Shell (Root)** | lxc exec [name] -- /bin/bash[cite: 23] |
| **Run Single Command** | lxc exec [name] -- apt update[cite: 23] |
| **Copy File TO Container** | lxc file push [local_path] [name]/[remote_path][cite: 23] |
| **Pull File FROM Container** | lxc file pull [name]/[remote_path] [local_path][cite: 23] |
| **Edit Config** | lxc config edit [name][cite: 23] |
| **Set Resource Limit** | lxc config set [name] limits.cpu 2[cite: 23] |

## **📸 Snapshots & Images**
One of the best features of LXC is the ability to "freeze" a state before making risky changes[cite: 23].
  - **Create Snapshot:** lxc snapshot [name] [snap_name][cite: 23]
  - **Restore Snapshot:** lxc restore [name] [snap_name][cite: 23]
  - **List Snapshots:** lxc info [name] (Look under the Snapshots section)[cite: 23]
  - **Delete Snapshot:** lxc delete [name]/[snap_name][cite: 23]
  - **Publish as Image:** lxc publish [name]/[snap_name] --alias [my-custom-image][cite: 23]
## **🌐 Network & Storage**
|  |  |
| :- | :- |
| Action | Command |
| **List Networks** | lxc network list[cite: 23] |
| **Show Network Details** | lxc network show [bridge_name][cite: 23] |
| **List Storage Pools** | lxc storage list[cite: 23] |
| **Create Managed Volume** | lxc storage volume create [pool] [volume_name][cite: 23] |

### **Comparison Note**
  - **Docker:** Temporary, ephemeral, application-centric[cite: 23].
  - **LXC/LXD:** Persistent, stateful, machine-centric (it has its own init, ssh, cron, etc.)[cite: 23].
Should we add a section for **Proxmox-specific LXC** commands (since many people use LXC through the Proxmox pct tool)?[cite: 23]
