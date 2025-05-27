# Ansible Ubuntu Webserver

A minimal Ansible repo that turns a fresh Ubuntu 20.04/22.04 VM into a basic Apache web server—in **seven** idempotent tasks. The variable file now shows examples of the five variable types your platform supports: **string, number, boolean, password, and domain**.

---

## Tasks performed
1. Update the APT cache  
2. Upgrade all packages  
3. Install Apache & UFW  
4. Deploy a templated `index.html`  
5. Ensure Apache is enabled and running  
6. Open HTTP (80) & HTTPS (443) in UFW  
7. Create an admin user with sudo privileges

---

## Prerequisites
* Ansible 2.15+ on your control machine (Linux/macOS/WSL)  
* An Ubuntu VM reachable via SSH (20.04 or 22.04)  
* SSH key‑based or password authentication

---

## Quick Start
```bash
git clone https://github.com/youruser/ansible-ubuntu-webserver.git
cd ansible-ubuntu-webserver
```
# Edit inventory
nano inventory/hosts.ini

# (Optional) Adjust variables
nano group_vars/all.yml

# Run the playbook
ansible-playbook playbook.yml
