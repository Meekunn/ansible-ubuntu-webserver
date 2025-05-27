# Simple Nginx Ansible Playbook

Spin up a tiny static site on any Debian/Ubuntu VM in **7 tasks**.

## Quick start

```bash
git clone https://github.com/<you>/simple-nginx-ansible.git
cd simple-nginx-ansible
```

# Edit inventory/hosts.ini to point at your VM
ansible-playbook -i inventory/hosts.ini playbook.yml
