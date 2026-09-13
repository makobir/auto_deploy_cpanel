# auto_deploy_cpanel

Clone from Git on cPanel, then push from GitHub / Git Desktop and the site auto-updates — using `auto_deploy.php` + webhook.

---

## Overview

1. **SSH setup** — cPanel ↔ GitHub connection
2. **cPanel Git Version Control** — repo clone
3. **Webhook + `auto_deploy.php`** — auto deploy on every push

---

## Part 1: GitHub SSH Setup in cPanel

First you need to generate an SSH key, otherwise private repo clone / pull will fail.

### 1. Generate SSH key

In cPanel Terminal (or SSH):

```bash
ssh-keygen -t rsa -b 2048 -C "cpanel-username@yourdomain.com"
