# Ansible › Full Infrastructure Automation

This folder contains Ansible playbooks used to automate the provisioning and setup of a Kubernetes (K3s) cluster, Docker, Jenkins, monitoring, firewall, and reverse proxy—all part of my DevOps bootcamp final task.

**See details:** ([Ansible](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/tree/main/stage2/final-task/ansible))

---

## Contents

- `group_vars/…`: Host and group-level variables to customize playbooks
- `inventory`: Defines target hosts grouped by roles (e.g., master, worker)
- `ansible.cfg`: Configuration file for paths and settings
- `main.yaml`: Entry-playbook that orchestrates the full workflow
- Playbooks:
  1. `1install_docker.yaml` — Installs Docker engine on all nodes
  2. `2create_user.yaml` — Creates a non-root user and configures sudo access
  3. `3setup_ufw.yaml` — Configures UFW firewall rules
  4. `4install_mon.yaml` — Installs monitoring stack (Prometheus/Grafana)
  5. `5reverse_proxy.yaml` — Sets up NGINX reverse proxy with SSL
  6. `6clone_repo.yaml` — Retrieves application code from GitHub
  7. `7install_k3s.yaml` — Installs K3s cluster with Ansible
  8. `8install_jenkins.yaml` — Deploys Jenkins CI server

---

## How to Run

Execute the complete automation flow with:

```
ansible-playbook -i inventory main.yaml
```

## Summary
- Automated OS & Docker setup
- Enhanced security via user creation and firewalls
- Powered monitoring and CI/CD on the same infrastructure
- Rolled out Kubernetes with K3s and orchestrated Jenkins
- Delivered SSL-terminated applications via reverse proxy
