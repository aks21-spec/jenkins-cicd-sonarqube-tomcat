# Jenkins CI/CD Pipeline Setup Guide

## Components Used

- Jenkins
- GitHub
- Maven
- SonarQube
- Apache Tomcat

## Pipeline Flow

1. Developer pushes code to GitHub.
2. GitHub Webhook triggers Jenkins Pipeline.
3. Jenkins pulls source code.
4. Maven builds the application.
5. SonarQube performs code analysis.
6. Quality Gate validates code quality.
7. Jenkins deploys the WAR file to Apache Tomcat.
