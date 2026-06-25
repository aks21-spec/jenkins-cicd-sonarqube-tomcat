# CI/CD Architecture

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
Quality Gate
    |
Apache Tomcat
    |
Application Deployment
```

## Components

### GitHub
Stores application source code.

### GitHub Webhook
Automatically triggers Jenkins whenever code is pushed.

### Jenkins
Executes the CI/CD pipeline.

### Maven
Builds and packages the Java application.

### SonarQube
Performs static code analysis and quality checks.

### Quality Gate
Ensures code meets quality standards before deployment.

### Apache Tomcat
Hosts and runs the deployed application.
