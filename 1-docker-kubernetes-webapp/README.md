# Kubernetes Web App & Docker Registry Showcase

This folder presents my end-to-end DevOps work for the "dumbmerch"-app covering private Docker registry, multi-environment Docker deployments, and fully orchestrated Kubernetes deployment.

---

## 1. Docker Registry

I set up a **private Docker registry** using Docker Compose, including:
- `registry` service and a `frontend` UI for image browsing
- NGINX as a reverse proxy with SSL and HTTP basic auth protection
- Demonstrated pushing app images to the private registry
  *Screenshot of image push & registry UI included*

**See details:** [`docker-registry.md`](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/docker-registry.md)

---

## 2. Docker Compose Deployment

Deployed staging versions of frontend, backend, and PostgreSQL using Docker Compose:
- PostgreSQL container with host-mounted volume and remote connection enabled
- Optimized Dockerfiles:
  - Frontend: Node.js multi-stage build → NGINX
  - Backend: Go build + lightweight Alpine runtime
- Docker Compose file orchestrating app stack for staging
- Reference to Kubernetes-driven production load-balancing as covered later

**See details:** [`deployment.md`](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/deployment.md)

---

## 3. Production Kubernetes Deployment

Orchestrated production deployment on a K3s cluster configured via Ansible:
- PostgreSQL setup:
  - Secure credentials with `Secret`
  - Data persistence via `PersistentVolumeClaim` + `StatefulSet`
  - Service (NodePort) for external access
- Deployed frontend, backend, pgAdmin with `Deployments` and `Services` (LoadBalancer / NodePort)
- Enabled HA with HAProxy for database failover
- Cluster installation and exclusions (Traefik) automated via Ansible

**See details:** [`kubernetes.md`](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/kubernetes.md)

---
