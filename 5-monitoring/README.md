# Monitoring: Grafana & Prometheus

This folder contains the setting up monitoring and alerting for all servers and containers using Prometheus, Grafana, and Alertmanager:

## Related File

- [monitoring.md](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/monitoring.md)
- [Ansible playbook - install_mon.yaml](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/ansible/4install_mon.yaml)

## What I Did

- Installed Prometheus, Grafana, and Node Exporter using Ansible
- Secured Prometheus with Basic Auth via NGINX
- Connected Prometheus as Grafana data source
- Built custom Grafana dashboards to monitor:
  - Disk usage
  - Memory usage
  - CPU usage
  - Container resource usage
  - Network usage
- Integrated Telegram bot with Grafana alerting
- Created alert rules for:
  - High CPU usage
  - RAM usage
  - Free disk space
  - NGINX network I/O

## Result

All server and container metrics are now visualized and monitored via Grafana. Alerts are sent to Telegram when thresholds are exceeded.
