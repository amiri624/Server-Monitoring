# Server-Monitoring




---

🌐 DevOps Monitoring Stack

Prometheus | Grafana | Node Exporter | Ansible Automation | GitHub Actions CI/CD

A fully automated and production-ready monitoring stack for Linux servers using Prometheus, Grafana, and Node Exporter, deployed and managed with Ansible and automatically delivered via GitHub Actions CI/CD.

This project is designed to demonstrate real, practical DevOps skills including:
✔️ Automation
✔️ Configuration Management
✔️ Infrastructure Monitoring
✔️ CI/CD Pipelines
✔️ Docker-based local environments

Perfect for production usage and for showcasing in your DevOps portfolio.


---

📊 Architecture Overview

┌──────────────────────────┐
        │        GitHub Repo       │
        │  ──────────┬──────────   │
        └────────────┼─────────────┘
                     │ (push)
                     ▼
            ┌───────────────────┐
            │ GitHub Actions CI │
            │  deploy.yml       │
            └───────┬──────────┘
                    │ SSH
                    ▼
      ┌────────────────────────────────┐
      │         Target Server          │
      │────────────────────────────────│
      │  Ansible Roles Deploy:         │
      │   • Prometheus                 │
      │   • Node Exporter              │
      │   • Grafana                    │
      │________│
                    │
                    ▼
    ┌────────────────────────────────────┐
    │  Monitoring Stack                  │
    │  • Prometheus  (9090)              │
    │  • Grafana      (3000)             │
    │  • NodeExporter (9100)             │
    └────────────────────────────────────┘


---

📁 Project Structure

devops-monitoring/
│
├── ansible.cfg
├── inventory/
│   └── hosts.ini
├── playbooks/
│   └── site.yml
├── roles/
│   ├── prometheus/
│   ├── grafana/
│   └── node_exporter/
├── prometheus/
│   └── prometheus.yml
├── files/
│   └── grafana_dashboards/
│       └── system_metrics.json
├── docker-compose.yml
├── .github/
│   └── workflows/
│       └── deploy.yml
├── .gitignore
└── README.md


---

🚀 Features

🔧 Ansible Automation

Automated installation of Prometheus

Automated installation of Grafana

Automated installation of Node Exporter

Systemd service management

Template-based configuration


📈 Monitoring Stack

Prometheus

Grafana

Node Exporter

Custom, ready-to-import Grafana dashboard


🐳 Local Docker Environment

One-command startup using Docker Compose

Ideal for development or testing


🤖 CI/CD Pipeline (GitHub Actions)

Automatic deployment to any server

Secure SSH via GitHub Secrets

Zero manual interaction after setup



---

🛠 Manual Deployment (Ansible)

1. Add your server to:



inventory/hosts.ini

2. Run the playbook:



ansible-playbook playbooks/site.yml -i inventory/hosts.ini


---

🐳 Local Deployment via Docker Compose

Start everything:

docker-compose up -d

Access services:

Service URL

Grafana http://localhost:3000
Prometheus http://localhost:9090
Node Exporter http://localhost:9100/metrics



---

📊 Grafana Dashboard

Import:

files/grafana_dashboards/system_metrics.json

Dashboard includes:

CPU Usage

Memory Usage

Disk Usage

Network RX/TX Traffic



---

🔐 CI/CD Setup (GitHub Actions)

Add these secrets in:

GitHub → Settings → Secrets → Actions

Secret Description

SSH_PRIVATE_KEY Private SSH key
SERVER_USER SSH username
SERVER_IP Server IP address


Pipeline runs automatically on:

✔️ Push to main
✔️ Manual dispatch


---

⚙️ Technologies Used

Ansible

Prometheus

Grafana

Node Exporter

Docker & Docker Compose

GitHub Actions

Linux Systemd

YAML

Bash



---

🎯 Why This Project is Good for a DevOps Portfolio?

Shows real-world automation

Includes CI/CD pipeline

Includes server provisioning

Includes monitoring stack

Includes templates & services

Shows folder organization best-practices

Looks highly professional to recruiters
