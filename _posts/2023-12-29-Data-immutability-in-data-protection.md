---
layout: post
title:  Data Immutability in Data Protection
date: 2023-12-29 06:00:00
description: securing access to backed-up data
tags: data-protection
categories: Retention-Lock
---

# Data Immutability in Data Protection

Data immutability is a critical aspect of data protection. It involves securing stored data on a protection device in a way that prevents unauthorized alterations or updates. The retention lock concept plays a pivotal role in achieving this security. Retention lock allows data to be locked for a specific duration, during which no user or intruder can modify the locked data until the lock expires.

## Forms of Retention Lock

1. **Compliance Lock:**
   Once enabled, this lock on data cannot be reversed. It is the strictest form, preventing the unlocking of data until the lock's expiration.

2. **Governance Lock:**
   A less strict form wherein data remains locked until the specified time duration ends or until an administrator disables the lock.

3. **Auto Retention Lock:**
   Also known as the default retention lock, data is locked immediately upon backup and remains locked until a set cool-off period expires.

4. **Indefinite Retention Lock:**
   This lock keeps data locked indefinitely, useful for compliance or during legal disputes until resolution. Once enabled, the data remains locked without an expiry or until the cooling-off period ends.

## Attack Vectors on Backed-up Data

Several attack vectors or techniques can be employed to exploit backed-up or locked data:

1. **Namespace Level Protection:**
   Protects data within the file system namespace, preventing operations like renaming, modification, or deletion.

2. **Clock Manipulation and NTP Servers:**
   Attacker manipulation of server clocks or NTP access can alter retained data by adjusting time and date settings.

3. **Backdoor Access via OS Shell:**
   Access to the backup system's OS shell can allow an attacker to execute destructive commands on the data.

4. **Hypervisor Level Access:**
   Inadequately secured hypervisor consoles grant access to data stores and virtual machine networks, enabling destructive commands.

5. **Bootloader Level Access:**
   Unsecured OS bootloaders provide direct access to the shell, making data vulnerable to exploitation.

6. **BIOS and Platform Management Interface:**
   Unsecured interfaces provide remote access to the system, potentially compromising data stored on disks.

7. **Data Center Access:**
   Physical access to data centers allows attackers to destroy or manipulate data on disks.

## Hardening Practices for Enhanced Security

To strengthen system security, consider implementing the following practices:

- Restrict physical access to unauthorized personnel.
- Disconnect BIOS and platform management interfaces from the network. Randomize root credentials and implement temporary user logins for specific durations.
- Secure bootloaders by randomizing root passwords and restricting the ability to edit bootloader entries.
- Secure the OS shell by limiting user access to non-destructive commands or implementing time-based token access.
- Secure the hypervisor by blocking external access and tools like CLI, GUI, and ipmitool.
- Implement measures to secure clock and NTP settings by restricting frequency and number of modifications, requiring 2FA during NTP configurations, and enabling secure NTP to detect clock skew.

These practices can significantly enhance the security of your system against potential attacks on backed-up data.
