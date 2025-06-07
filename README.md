# Born2beRoot

> *"Because setting up a secure Linux server should be painful... and educational."*

## 📌 Project Overview

**Born2beRoot** is a system administration project from the 42 Common Core that introduces virtualization, Linux server management, and basic security practices. The objective is to configure a virtual machine running Debian (or Rocky Linux) with strict security and system rules, following a series of mandatory steps to build a minimal, secure, and functional server environment.

## 💻 What I Had to Do

* Set up a **Virtual Machine** using VirtualBox (I used Debian).
* Partition the disk with **LVM encryption**.
* Configure **UFW firewall** and ensure only port 4242 is open.
* Set up and secure **SSH** (no root login!).
* Create and manage users and groups with proper **password policies**.
* Configure **sudo rules** and enable **logging** for all sudo actions.
* Write a **Bash script (monitoring.sh)** that displays live system stats every 10 minutes on all terminals.

## 🧠 What I Learned

### Linux Basics & System Setup

I learned how to install and configure a Linux system from scratch, without a graphical interface. It taught me how to navigate the command line efficiently and how Linux handles services, users, permissions, and networking.

### Security Practices

This project introduced me to essential server hardening techniques:

* Blocking root SSH access
* Enforcing password complexity
* Restricting sudo privileges
* Using a firewall (UFW)
* Monitoring user commands

### Disk Partitioning & LVM

Setting up encrypted partitions with LVM was completely new to me. I now understand what logical volumes are, how to manage them, and why encryption matters in server environments.

### Scripting & Automation

Writing `monitoring.sh` helped me practice real-world Bash scripting. I learned about:

* Using `wall` to broadcast messages
* Parsing CPU, memory, and disk usage
* Scheduling scripts with `cron`

## 😓 Challenges I Faced

### Enforcing Password Policy

Configuring PAM modules for password complexity and expiration rules took a lot of trial and error. Reading logs and understanding why a password was rejected helped me dive into PAM and system authentication internals.

### Sudo Configuration

Setting up sudo with custom log paths, TTY requirement, and restricted environment variables was tricky. I had to be very cautious because a misconfiguration could lock me out or break sudo entirely.

### Understanding System Tools

Tools like `lsblk`, `hostnamectl`, `ufw`, `journalctl`, and `crontab` became second nature by the end. Early on, I often confused their options or misunderstood their output, but practice helped.

### Logging with Bash

Capturing and formatting system information correctly in the `monitoring.sh` script was harder than expected. I had to account for output formats, arithmetic operations in Bash, and permissions.

## 🧾 Submission

Only a single `signature.txt` file is submitted. This file contains the SHA1 signature of the VM’s disk image. No VM or configuration files are submitted — everything is tested live during the defense.

## 📚 Resources That Helped

* [Debian Wiki](https://wiki.debian.org/)
* [Arch Linux Manual Pages](https://man.archlinux.org/)
* `man sudoers`, `man passwd`, `man pam_pwquality`
* YouTube videos on LVM, PAM, and SSH configuration

---

## 🎯 Final Thoughts

Born2beRoot was one of the most hands-on and rewarding projects at 42. It pushed me out of my comfort zone and into the world of real system administration. While it wasn’t the easiest experience, I now feel more confident working with Linux, writing scripts, and thinking critically about system security.
