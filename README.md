# Ansible Ubuntu Webserver

This repository contains a simple Ansible playbook that provisions an Apache web server on Ubuntu with **seven** clearly defined tasks.

## Tasks performed
1. Update the APT cache  
2. Upgrade all packages  
3. Install Apache & UFW  
4. Deploy a custom `index.html` from a Jinja2 template  
5. Ensure Apache is enabled and running  
6. Configure UFW to allow HTTP (80) & HTTPS (443)  
7. Create an admin user with sudo privileges

## Prerequisites
* Ansible 2.15+ on your control machine (Linux/macOS/WSL)  
* A target VM running **Ubuntu 20.04 / 22.04** reachable via SSH  
* SSH key‑based access (password works too—configure in `hosts.ini`)

## Quick Start
```bash
git clone https://github.com/youruser/ansible-ubuntu-webserver.git
cd ansible-ubuntu-webserver

# Edit inventory
nano inventory/hosts.ini

# (Optional) Adjust variables
nano group_vars/all.yml

# Run the playbook
ansible-playbook playbook.yml
