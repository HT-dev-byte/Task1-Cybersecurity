# Linux Cheat Sheet

A practical guide to essential Linux command line operations for system administration and security operations.

---

## File & Directory Operations

| Command | Description | Example |
| :--- | :--- | :--- |
| `pwd` | Show current working directory path | `pwd` |
| `ls` | List files and directories in current or specified path | `ls -la /var/log` |
| `cd` | Change directory | `cd /etc/network` |
| `mkdir` | Create new directory (use `-p` for parent directories) | `mkdir -p lab/screenshots` |
| `cp` | Copy files or directories (`-r` for recursive) | `cp config.conf config.conf.bak` |
| `mv` | Move or rename files and directories | `mv target.txt /tmp/` |
| `rm` | Remove files or directories (`-rf` for recursive force) | `rm -rf old_data/` |

---

## Permissions & Ownership

| Command | Description | Example |
| :--- | :--- | :--- |
| `chmod` | Change file permissions (octal or symbolic) | `chmod 755 script.sh` |
| `chown` | Change file owner and group | `chown kali:kali report.md` |

---

## Package Management

| Command | Description | Example |
| :--- | :--- | :--- |
| `apt` | Advanced Package Tool for Debian-based systems | `sudo apt update && sudo apt install nmap` |
| `dpkg` | Low-level Debian package manager | `sudo dpkg -i package.deb` |

---

## Networking & Troubleshooting

| Command | Description | Example |
| :--- | :--- | :--- |
| `ip addr` | Display or configure network interfaces and IP addresses | `ip addr show eth0` |
| `ping` | Test network reachability and packet response time | `ping -c 4 192.168.56.101` |
| `ss` | Display network socket status and listening ports | `ss -tuln` |
| `traceroute` | Trace path and hops packets take to reach network target | `traceroute 8.8.8.8` |

---

## Quick Reference Summary

```bash
# System info & navigation
pwd
ls -la
cd /var/www/html

# Managing files
mkdir -p project/notes
cp -r project/ backup/
mv file.txt renamed.txt
rm -i unwanted.txt

# Permissions
chmod +x exploit.py
sudo chown root:root /etc/shadow

# Network checks
ip addr
ping -c 4 192.168.56.1
ss -tulpn
traceroute google.com
```
