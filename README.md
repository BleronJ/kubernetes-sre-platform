# Kubernetes SRE Platform

**A hands-on Site Reliability Engineering and Cloud Infrastructure project.**

The goal of this project is to design, deploy, monitor, secure, and troubleshoot a production-style application running on Kubernetes.

This project is part of my journey to deepen my expertise in Kubernetes, cloud infrastructure, automation, observability, and Site Reliability Engineering (SRE).

Rather than focusing only on deploying applications, the project emphasizes understanding system behavior, identifying failures, improving reliability, and automating operational tasks.

## Objectives

- Develop a deeper understanding of Kubernetes and container orchestration.
- Build repeatable infrastructure using Infrastructure as Code (IaC).
- Implement CI/CD pipelines for automated testing and deployment.
- Monitor application health, performance, and resource utilization.
- Use Prometheus and Grafana for metrics, dashboards, and alerting.
- Practice incident investigation, troubleshooting, and recovery.
- Apply security best practices, including least-privilege access and secure secrets management.
- Compare Kubernetes deployments across AWS, Google Cloud, and Microsoft Azure.
- Document engineering decisions, trade-offs, and lessons learned.

## Planned Technology Stack

| Area | Technologies |
|---|---|
| Application | Python, FastAPI |
| Containers | Docker |
| Orchestration | Kubernetes |
| Local development | kind |
| Cloud infrastructure | AWS, Google Cloud, Microsoft Azure |
| Infrastructure as Code | Terraform |
| CI/CD | GitHub Actions |
| Monitoring | Prometheus |
| Dashboards | Grafana |
| Version control | Git and GitHub |

Technologies will be introduced progressively as the project evolves.

## Architecture

The initial architecture will consist of a small API running inside a local Kubernetes cluster.

```text
Developer
    |
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    v
Build and Validate
    |
    v
Container Image
    |
    v
Kubernetes Cluster
    |
    +---- API Deployment
    |
    +---- Kubernetes Service
    |
    +---- Health Checks
    |
    +---- Prometheus
              |
              v
           Grafana
```

The architecture will evolve to include cloud infrastructure, automated deployments, alerting, and reliability testing.

## Project Roadmap

### Phase 1 — Application and Kubernetes Fundamentals
- Build a basic API with health-check endpoints.
- Write unit tests and containerize the application.
- Deploy the application to a local Kubernetes cluster using kind.
- Learn Pods, Deployments, Services, ConfigMaps, and health probes.

### Phase 2 — CI/CD and Automation
- Create GitHub Actions workflows.
- Automate tests, container builds, and Kubernetes manifest validation.
- Introduce image scanning and deployment validation.
- Practice versioning and rollback procedures.

### Phase 3 — Observability and Reliability
- Integrate Prometheus and Grafana.
- Monitor request rates, errors, latency, and resource utilization.
- Define service-level indicators and an initial service-level objective.
- Create actionable alerts and investigate simulated failures.

### Phase 4 — Cloud Infrastructure
- Provision infrastructure using Terraform.
- Deploy the application to Amazon EKS.
- Learn AWS IAM, networking, container registries, and Kubernetes access management.
- Evaluate the costs of cloud resources and clean up unused infrastructure.

### Phase 5 — Multi-Cloud Exploration
- Explore equivalent deployments on Google Kubernetes Engine (GKE) and Azure Kubernetes Service (AKS).
- Separate portable Kubernetes configurations from provider-specific infrastructure.
- Compare identity, networking, monitoring, security, and operational trade-offs.

### Phase 6 — SRE Practices
- Simulate application and infrastructure failures.
- Investigate incidents using logs, metrics, and Kubernetes events.
- Document root causes, remediation, and prevention measures.
- Test recovery, deployment rollback, and resource scaling.

## Engineering Principles

- **Automation first:** automate repetitive and error-prone tasks.
- **Reliability:** design for failure and validate recovery.
- **Observability:** use evidence from metrics, logs, and events to investigate issues.
- **Security:** follow least privilege and avoid committing secrets.
- **Reproducibility:** document how to build, deploy, test, and clean up the environment.
- **Cost awareness:** estimate cloud costs before provisioning resources.
- **Continuous improvement:** document lessons learned and improve the platform incrementally.

## Repository Structure

The repository will evolve toward the following structure:

```text
kubernetes-sre-platform/
├── app/
├── tests/
├── docker/
├── kubernetes/
├── terraform/
│   ├── aws/
│   ├── gcp/
│   └── azure/
├── monitoring/
│   ├── prometheus/
│   └── grafana/
├── .github/
│   └── workflows/
└── README.md
```

Directories will be added as the corresponding components are implemented.

## Cost Management

Development will begin locally to minimize costs.

Cloud deployments will be introduced only when necessary. AWS Free Tier eligibility, EKS pricing, and other resource charges will be reviewed before provisioning infrastructure.

Budgets and billing alerts will be configured where available, and temporary resources will be removed after experiments.

## Project Status

**Current stage:** Project initialization.

The initial focus is on building the application, understanding Kubernetes fundamentals, and establishing a repeatable development workflow.

Features will be marked as completed only after implementation and validation.

---

**Long-term goal:** Build a reproducible, observable, and reliable Kubernetes platform that demonstrates practical cloud infrastructure engineering and SRE principles.