Here is a quick reference cheat sheet for **UFW (Uncomplicated Firewall)** on Ubuntu/Debian systems[cite: 26].
Service Control & Status
|  |  |
| :- | :- |
| **Command** | **Action** |
| sudo ufw status | View firewall status (enabled/disabled)[cite: 26] |
| sudo ufw status verbose | View detailed status, default policies, and active rules[cite: 26] |
| sudo ufw status numbered | Display active rules with line numbers (useful for deletion)[cite: 26] |
| sudo ufw enable | Enable UFW (starts automatically on boot)[cite: 26] |
| sudo ufw disable | Disable UFW[cite: 26] |
| sudo ufw reload | Reload UFW rules without resetting connections[cite: 26] |
| sudo ufw reset | Reset UFW to default factory state (deletes all custom rules)[cite: 26] |

Default Policies
Set default traffic handling before adding specific rules[cite: 26]:
# Deny all incoming traffic and allow all outgoing traffic (standard baseline)  
sudo ufw default deny incoming[cite: 26]  
sudo ufw default allow outgoing[cite: 26]  
Allowing Traffic
By Port or Service
# Allow SSH by service name or port number  
sudo ufw allow ssh[cite: 26]  
sudo ufw allow 22[cite: 26]  
  
# Allow HTTP and HTTPS  
sudo ufw allow http[cite: 26]  
sudo ufw allow https[cite: 26]  
sudo ufw allow 80/tcp[cite: 26]  
sudo ufw allow 443/tcp[cite: 26]  
By Port Range & Protocol
# Allow TCP port range 6000 to 6007  
sudo ufw allow 6000:6007/tcp[cite: 26]  
  
# Allow UDP port range 6000 to 6007  
sudo ufw allow 6000:6007/udp[cite: 26]  
By IP Address or Subnet
# Allow all incoming connections from a specific IP address  
sudo ufw allow from 192.168.1.50[cite: 26]  
  
# Allow a specific IP address on a specific port (e.g., SSH)  
sudo ufw allow from 192.168.1.50 to any port 22[cite: 26]  
  
# Allow an entire subnet (e.g., 192.168.1.0/24)  
sudo ufw allow from 192.168.1.0/24[cite: 26]  
  
# Allow an entire subnet to access a specific port (e.g., MySQL 3306)  
sudo ufw allow from 192.168.1.0/24 to any port 3306[cite: 26]  
Denying & Rate Limiting
# Deny incoming traffic on port 80  
sudo ufw deny 80/tcp[cite: 26]  
  
# Deny connections from a specific IP  
sudo ufw deny from 203.0.113.100[cite: 26]  
  
# Rate limit SSH (denies connections from IPs with 6+ attempts in 30 seconds)  
sudo ufw limit ssh[cite: 26]  
Deleting Rules
Method 1: By Rule Line Number
# 1. List rules with numbers  
sudo ufw status numbered[cite: 26]  
  
# 2. Delete rule by number (e.g., rule #3)  
sudo ufw delete 3[cite: 26]  
Method 2: By Original Syntax
sudo ufw delete allow 80/tcp[cite: 26]  
sudo ufw delete allow ssh[cite: 26]  
Network Interface Rules
Apply rules to specific network interfaces (e.g., eth0 or wg0)[cite: 26]:
# Allow incoming traffic on port 80 on eth0 only  
sudo ufw allow in on eth0 to any port 80[cite: 26]  
  
# Allow traffic on a specific VPN interface  
sudo ufw allow in on wg0[cite: 26]  
Logging
# Enable logging (logs stored in /var/log/ufw.log)  
sudo ufw logging on[cite: 26]  
  
# Set logging level (low, medium, high, full)  
sudo ufw logging medium[cite: 26]  
  
# Disable logging  
sudo ufw logging off[cite: 26]
