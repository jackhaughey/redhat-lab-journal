# RHCSA Labs

A hands-on lab repository documenting my preparation for the Red Hat Certified System Administrator (RHCSA) certification.

This repository contains practical exercises, challenge scenarios, troubleshooting notes, and exam-style labs completed on Red Hat Enterprise Linux.

The goal is to build demonstrable Linux administration skills while creating a repeatable reference and study resource.

---

## Skills Covered

### Essential Tools

- Shell usage
- File management
- Permissions
- SSH
- grep and regular expressions
- Archiving and compression

### Software Management

- RPM packages
- DNF repositories
- Flatpak

### Shell Scripting

- Variables and arguments
- Conditional logic
- Loops
- Command substitution

### System Operations

- systemd
- Journald
- Process management
- Boot targets
- System recovery

### Storage

- GPT partitioning
- LVM
- Swap management

### File Systems

- XFS
- ext4
- NFS
- autofs

### Networking

- IPv4
- IPv6
- NetworkManager
- firewalld
- Troubleshooting

### User Administration

- Users and groups
- Password policies
- Sudo configuration

### Security

- SELinux
- SSH key authentication
- Firewall administration

---

## Repository Structure

```text
rhcsa-labs/
│
├── 01-essential-tools/
├── 02-package-management/
├── 03-shell-scripting/
├── 04-system-operations/
├── 05-storage/
├── 06-filesystems/
├── 07-services/
├── 08-networking/
├── 09-users-groups/
├── 10-selinux/
└── challenge-labs/
```

Each section contains:

- Objective
- Lab steps
- Verification commands
- Troubleshooting notes
- Lessons learned

---

## Lab Environment

| Component | Value |
|-----------|---------|
| Operating System | Red Hat Enterprise Linux |
| Virtualisation | VMware / VirtualBox |
| Shell | Bash |
| Networking | NetworkManager |
| Firewall | firewalld |
| Security | SELinux |

---

## Progress Tracker

| Section | Status |
|----------|----------|
| Essential Tools | ⬜ |
| Package Management | ⬜ |
| Shell Scripting | ⬜ |
| System Operations | ⬜ |
| Storage | ⬜ |
| File Systems | ⬜ |
| Services | ⬜ |
| Networking | 🟨 In Progress |
| Users & Groups | ⬜ |
| SELinux | ⬜ |
| Mock Exam | ⬜ |

Legend:

- ⬜ Not Started
- 🟨 In Progress
- ✅ Completed

---

## Challenge Labs

The repository includes exam-style scenarios designed to simulate RHCSA troubleshooting tasks.

Examples include:

- Web server inaccessible
- Broken network connectivity
- Firewall and SELinux conflicts
- Storage expansion requests
- User access issues

---

## Exam Philosophy

Red Hat certifications are performance based.

Every lab in this repository follows the same principle:

1. Configure the system.
2. Verify functionality.
3. Ensure the configuration survives reboot.
4. Document troubleshooting and recovery procedures.

---

## Future Enhancements

Beyond RHCSA objectives:

- Podman containers
- Ansible automation
- Network namespaces
- Linux troubleshooting scenarios
- RHCE preparation
- OpenShift foundations

---

## Author

Jack Haughey

Telecommunications and Network Operations Engineer exploring Linux, automation, platform engineering and cloud-native technologies.
