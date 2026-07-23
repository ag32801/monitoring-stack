# Containerized Infrastructure Monitoring Stack

A lightweight, production-ready monitoring setup built with **Prometheus**, **Grafana**, **Node Exporter**, and **Blackbox Exporter** using Docker Compose.

---

## 🛠 Features
- **Host Resource Tracking:** Live metrics for CPU, RAM, Disk, and Network usage via Node Exporter.
- **ICMP Ping Monitoring:** Real-time uptime and network latency tracking for local network devices via Blackbox Exporter.
- **Alerting Ready:** Pre-configured SMTP environment variables for Grafana email notifications.
- **Secure Secret Handling:** Secrets are decoupled using environment variables (`.env`) and excluded from Git tracking.

---

## 📁 Repository Structure

```text
monitoring/
├── .env                  # Local secrets (ignored by Git)
├── .env.example          # Template for environment variables
├── .gitignore            # Git ignore rules
├── README.md             # Project documentation
├── docker-compose.yml    # Container orchestration services
└── prometheus/
    └── prometheus.yml    # Prometheus scrape targets configuration
