# Containerized Infrastructure Monitoring Stack

A lightweight, production-ready monitoring setup built with **Prometheus**, **Grafana**, **Node Exporter**, and **Blackbox Exporter** using Docker Compose.

## Features
- **Host Resource Tracking:** Live metrics for CPU, RAM, Disk, and Network usage.
- **ICMP Ping Monitoring:** Real-time uptime and network latency tracking for IPs.
- **Alerting Ready:** Pre-configured SMTP settings for Grafana email notifications.

## Quick Start Guide

1. Clone the repository and navigate into the folder:
   ```bash
   cd monitoring
   ```

2. Set up your secret variables:
   ```bash
   cp .env.example .env
   ```
   *(Edit `.env` to add your actual Grafana password and Google App Password).*

3. Launch the stack:
   ```bash
   docker compose up -d
   ```

4. Access Grafana:
   - **URL:** `http://localhost:3000`
   - **User:** `admin`
   - **Recommended Dashboards to Import:** 
     - Node Exporter: **`1860`**
     - Blackbox Ping Exporter: **`7587`**