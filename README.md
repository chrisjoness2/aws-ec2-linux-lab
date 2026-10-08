# AWS EC2 Linux Administration & Troubleshooting Lab

## Overview

Hands-on AWS EC2 and Linux administration lab focused on remote server access, AWS networking, security groups, Linux permissions, process management, and troubleshooting.

Launched an Ubuntu Linux EC2 instance, connected through SSH, practiced Linux administration, and intentionally tested and restored SSH connectivity by modifying Security Group rules.

The EC2 instance was terminated after the lab to avoid unnecessary AWS costs.

## AWS Services & Tools

- Amazon EC2
- Amazon VPC
- Security Groups
- SSH
- Ubuntu Linux
- AWS Management Console
- macOS Terminal

## Architecture

```text
Mac Terminal
     │
     │ SSH
     ▼
Internet
     │
     ▼
AWS Security Group
     │
     │ TCP 22
     ▼
EC2 Ubuntu Linux
```

## EC2 Configuration

- Ubuntu 24.04 LTS
- 64-bit x86
- t2.nano
- Default VPC
- 8 GiB GP3 storage
- SSH access through port 22
- SSH restricted to My IP

## Linux Administration

Practiced:

- Linux directory and file management
- File ownership and permissions
- `chmod`
- Process management with `ps`
- Process termination with `kill`
- Basic Linux troubleshooting

## Security Group Troubleshooting

Tested SSH connectivity by temporarily removing the inbound SSH rule from the Security Group.

After disconnecting from the instance, a new SSH connection resulted in:

```text
Operation timed out
```

Restored the SSH rule for port 22 from My IP and successfully reconnected.

This demonstrated how AWS Security Group configuration can directly affect EC2 connectivity.

## Key Concepts

- EC2 virtual machines
- Linux server administration
- SSH remote access
- Public vs. private IP addresses
- AWS Security Groups
- Linux permissions
- Process management
- Cloud troubleshooting

## Cleanup

The EC2 instance was terminated after completing the lab to prevent unnecessary ongoing charges.

The SSH private key was kept locally and excluded from Git using `.gitignore`.

## Skills Demonstrated

**AWS:** EC2, VPC, Security Groups, networking fundamentals
**Linux:** SSH, permissions, processes, troubleshooting
**Tools:** AWS Console, macOS Terminal, Git, GitHub
