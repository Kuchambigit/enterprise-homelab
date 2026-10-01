# Lesson 1 - Expanding an LVM Root Filesystem

## Objective

Expand the Ubuntu root filesystem after increasing the virtual disk size in Proxmox.

## Before

- Disk Size: 15 GB
- Used: 14 GB
- Free: 571 MB
- Usage: 96%

## Commands Used

- lsbk
- sudo vgs
- sudo lvs
- sudo lvextend -l +100%FREE -r /dev/ubuntu-vg/ubuntu-lv
- df -h

## After

- Disk Size: 30 GB
- Used: 14 GB
- Free: 15 GB
- Usage: 48%

## What I learned

...
