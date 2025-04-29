# 🚀 SLA-Driven DevOps for Multi-Service eCommerce Platform

This repository supports the final year project titled **“Designing SLA based on DevOps pipelines in a Project Driven Environment”**. It demonstrates how to integrate Service Level Agreements (SLAs) into DevOps pipelines using CI/CD, Docker, Prometheus, and Grafana.

## 🧠 Project Overview

Modern DevOps practices aim to deliver fast, reliable, and scalable software. However, aligning these practices with measurable SLAs remains a challenge. This project addresses that gap by embedding SLA monitoring and enforcement directly into a CI/CD pipeline, ensuring operational compliance and system reliability.

## 📦 Tech Stack

- **Backend Services**: Node.js (Express)
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus & Grafana
- **Orchestration-ready**: Kubernetes compatible
- **Version Control**: Git

## 🏗️ Repository Structure

```bash
mydevops/
├── auth-service/         # Handles user authentication
├── payment-service/      # Manages transactions and payment logic
├── product-service/      # Deals with product catalog and inventory
├── order-service/        # Handles order lifecycle
├── .github/workflows/    # GitHub Actions CI/CD definitions
├── prometheus/           # Monitoring config (prometheus.yml)
├── grafana/              # Grafana dashboards setup
├── docker-compose.yml    # For local multi-service orchestration
└── README.md             # Project documentation
