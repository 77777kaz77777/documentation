## **Package Management Cheat Sheet**
This table covers the essential commands for managing software[cite: 25]. Whether you're using **Debian/Ubuntu** (APT), **RHEL/Fedora/Rocky** (DNF), or **Arch** (Pacman), these are your bread-and-butter commands[cite: 25].
|  |  |  |  |
| :- | :- | :- | :- |
| Action | Debian / Ubuntu | RHEL / CentOS / Fedora | Arch Linux |
| **Update Repos** | sudo apt update[cite: 25] | sudo dnf check-update[cite: 25] | sudo pacman -Sy[cite: 25] |
| **Upgrade System** | sudo apt upgrade[cite: 25] | sudo dnf upgrade[cite: 25] | sudo pacman -Syu[cite: 25] |
| **Install Package** | sudo apt install [pkg][cite: 25] | sudo dnf install [pkg][cite: 25] | sudo pacman -S [pkg][cite: 25] |
| **Remove Package** | sudo apt remove [pkg][cite: 25] | sudo dnf remove [pkg][cite: 25] | sudo pacman -R [pkg][cite: 25] |
| **Search for Pkg** | apt search [query][cite: 25] | dnf search [query][cite: 25] | pacman -Ss [query][cite: 25] |
| **Clean Cache** | sudo apt autoremove[cite: 25] | sudo dnf clean all[cite: 25] | sudo pacman -Sc[cite: 25] |
| **Show Info** | apt show [pkg][cite: 25] | dnf info [pkg][cite: 25] | pacman -Si [pkg][cite: 25] |

## **System Maintenance & Info**
While many core commands (like ls, cd, grep) are universal, the way these systems handle services and identification can vary slightly[cite: 25].
### **Service Management (Systemd)**
*Most modern versions of all these distros use systemctl, so these are largely universal now:*[cite: 25]
  - **Start a service:** sudo systemctl start [service][cite: 25]
  - **Enable on boot:** sudo systemctl enable [service][cite: 25]
  - **Check status:** systemctl status [service][cite: 25]
### **System Identification**
If you forget which box you're logged into, use these[cite: 25]:
  - **Universal:** cat /etc/os-release[cite: 25]
  - **Debian/Ubuntu specific:** lsb_release -a[cite: 25]
  - **Red Hat specific:** cat /etc/redhat-release[cite: 25]
## **Key Differences at a Glance**
  - **Debian/Ubuntu:** Uses .deb packages[cite: 25]. Known for stability (Debian) and user-friendliness (Ubuntu)[cite: 25].
  - **RHEL/Fedora:** Uses .rpm packages[cite: 25]. Fedora is the "bleeding edge" upstream for the rock-solid Red Hat Enterprise Linux[cite: 25].
  - **Arch Linux:** Uses a "rolling release" model[cite: 25]. You install it once and update forever; there are no "major versions" like Ubuntu 24.04[cite: 25].
  - **The AUR:** Arch users have access to the **Arch User Repository**, a massive community-driven library usually accessed via a "helper" like yay (e.g., yay -S [package])[cite: 25].
