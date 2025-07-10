# NGINX Reverse Proxy & SSL Setup

This folder sets up a reverse proxy using NGINX and configures automatic SSL renewal using Certbot with wildcard certificates.

**Related Script:**
[5reverse_proxy.yaml (Ansible)](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/ansible/5reverse_proxy.yaml)

---

## Features

- NGINX reverse proxy setup via Ansible
- Wildcard SSL certificate using Certbot + Cloudflare DNS
- Automatic SSL renewal via cronjob
- Reverse proxy for multiple subdomains:
  - `fadil.studentdumbways.my.id` (Frontend App)
  - `api.fadil.studentdumbways.my.id` (Backend API)
  - `exporter.fadil.studentdumbways.my.id` (Node Exporter)
  - `prom.fadil.studentdumbways.my.id` (Prometheus)
  - `monitoring.fadil.studentdumbways.my.id` (Grafana)
  - `registry.fadil.studentdumbways.my.id` (Docker Registry)

---

## Auto SSL Renewal

A bash script (`renew_cert.sh`) is created to renew certificates using Certbot in Docker and reload NGINX after renewal.

```
0 2 * * 0 /home/finaltask-fadil/nginx/renew_cert.sh >> /home/finaltask-fadil/nginx/cert-renewal.log 2>&1
```
