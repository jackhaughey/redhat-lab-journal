# RHCSA Networking Labs
 
This section covers the networking objectives for the Red Hat Certified System Administrator (RHCSA) exam.
 
The focus is on configuring and troubleshooting networking using tools commonly used in Red Hat Enterprise Linux, including:
 
- nmcli
- ip
- hostnamectl
- NetworkManager
- firewalld
- firewall-cmd
 
All configurations should persist across reboots unless otherwise stated.
 
---
 
## RHCSA Objectives Covered
 
- Configure IPv4 addresses
- Configure IPv6 addresses
- Configure hostname resolution
- Configure network services to start automatically
- Restrict network access using firewalld
- Troubleshoot common networking issues
 
---
 
## Recommended Lab Environment
 
| Component | Value |
|-----------|---------|
| OS | RHEL 10 |
| VM Count | 2 |
| Network | Internal Lab Network |
| Management Tool | NetworkManager |
 
Suggested topology:
 
Server A
 
192.168.56.10/24
 
Server B
 
192.168.56.20/24
 
Gateway
 
192.168.56.1
 
---
 
## Labs
 
### Core Labs
 
| Lab | Topic | Status |
|------|--------|---------|
| 01 | Static IPv4 Configuration with nmcli | ✅ |
| 02 | IPv6 Configuration |  |
| 03 | Hostname Resolution |  |
| 04 | Network Troubleshooting |  |
| 05 | Firewalld Basics |  |
| 06 | Firewalld Services and Ports |  |
| 07 | Persistent Network Configuration |  |
 
### Challenge Labs
 
| Lab | Scenario |
|------|----------|
| Challenge 01 | Web Server Not Reachable |
| Challenge 02 | Broken Network Connectivity |
| Challenge 03 | Firewall and SELinux Interaction |
 
---
 
## Skills Checklist
 
### IPv4
 
- [ ] View interface configuration
- [ ] Configure static addresses
- [ ] Configure default gateways
- [ ] Configure DNS settings
- [ ] Verify routing table
 
### IPv6
 
- [ ] Configure IPv6 addresses
- [ ] Configure IPv6 gateways
- [ ] Test IPv6 connectivity
 
### Hostname Resolution
 
- [ ] Configure hostname
- [ ] Modify `/etc/hosts`
- [ ] Verify name resolution
 
### Firewalld
 
- [ ] Add services
- [ ] Remove services
- [ ] Add ports
- [ ] Remove ports
- [ ] Save persistent configuration
- [ ] Verify active rules
 
### Troubleshooting
 
- [ ] Diagnose interface issues
- [ ] Diagnose routing issues
- [ ] Diagnose DNS problems
- [ ] Diagnose firewall blocks
- [ ] Verify service reachability
 
---
 
## Common Commands

```bash
ip addr
ip route
nmcli con show
hostnamectl
ping6
ss -tulpn
firewall-cmd --list-all
systemctl status NetworkManager
```
