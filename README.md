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

## ⚙️ Getting Started

Prerequisites
	•	Node.js
	•	Docker
	•	Git

## Clone the Repository in your terminal:

git clone https://github.com/XBLondon/mydevops.git
cd mydevops

## Running the Application Locally in your terminal:

docker-compose up --build

This will build all services and bring up Prometheus and Grafana.
	•	Grafana: http://localhost:3000
	•	Prometheus: http://localhost:9090

## Github Actions CI/CD

Each push or pull request triggers the CI/CD pipeline:
	•	Build & test each service
	•	Dockerize services
	•	Deploy using docker-compose (or push to a container registry)

## Sample Workflow File yaml:

# .github/workflows/devops.yml
name: CI/CD Pipeline

on: [push]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Set up Node
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm ci && npm run test
      - run: docker build -t xblondon/auth-service ./auth-service


## 📊 SLA Monitoring with Prometheus & Grafana

Prometheus scrapes metrics from each service and feeds them into Grafana dashboards to visualize:
	•	Uptime
	•	Response times
	•	Error rates

Alerts can be set up for SLA breaches (e.g., response time > 200ms).

## 🧪 Testing & Validation

	Unit tests: run via GitHub Actions
	•	Monitoring tests: validate performance against SLA metrics
	•	Load tests: using Apache JMeter/Postman (optional)

## 📌 Key Features

	End-to-end automation from code commit to deployment
	•	SLA-enforced CI/CD pipeline
	•	Real-time monitoring and alerting
	•	Modular microservices with Docker

## 📄 License

This project is for academic use under the MIT License.





