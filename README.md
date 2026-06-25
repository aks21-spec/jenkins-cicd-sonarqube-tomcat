# Jenkins CI/CD Pipeline with SonarQube and Tomcat

## Project Overview

This project demonstrates the implementation of an automated CI/CD pipeline using Jenkins, GitHub Webhooks, Maven, SonarQube, and Apache Tomcat.

Whenever code is pushed to GitHub, Jenkins automatically triggers the pipeline, performs build validation, executes code quality analysis using SonarQube, validates the Quality Gate, and deploys the application to Apache Tomcat.

---

## Architecture

```text
Developer
    |
GitHub Repository
    |
GitHub Webhook
    |
Jenkins Pipeline
    |
Maven Build
    |
SonarQube Analysis
    |
Quality Gate Validation
    |
Apache Tomcat
    |
Application Deployment
```

---

## Technologies Used

- Jenkins
- GitHub
- GitHub Webhooks
- Maven
- SonarQube
- Apache Tomcat
- Java
- Linux

---

## CI/CD Pipeline Stages

### 1. Source Code Checkout

Jenkins pulls source code from GitHub.

### 2. Build

Maven builds the application and generates WAR artifacts.

### 3. Code Quality Analysis

SonarQube scans the codebase and generates quality reports.

### 4. Quality Gate Validation

Pipeline waits for SonarQube Quality Gate results before proceeding.

### 5. Deployment

WAR file is automatically deployed to Apache Tomcat.

---

## Features Implemented

- Pipeline as Code using Jenkinsfile
- Automated CI/CD Workflow
- GitHub Webhook Triggering
- Maven Build Automation
- SonarQube Integration
- Quality Gate Enforcement
- Automated Tomcat Deployment

---

## Skills Demonstrated

- Continuous Integration (CI)
- Continuous Deployment (CD)
- Jenkins Pipeline Development
- SonarQube Administration
- Build Automation
- Linux Administration
- Deployment Automation

---

## Screenshots

Screenshots are currently unavailable because the original lab environment was decommissioned after project completion.

The Jenkins pipeline configuration, deployment workflow, and setup documentation have been preserved in this repository.

---

## Project Outcome

Successfully implemented an automated CI/CD pipeline that performs source code checkout, application build, code quality analysis, quality gate validation, and automated deployment to Apache Tomcat upon code changes pushed to GitHub.

---

## Future Improvements

- Docker Integration
- Kubernetes Deployment
- AWS Deployment Automation
- Infrastructure as Code using Terraform
- Monitoring using Prometheus and Grafana
