pipeline {
    agent any

    stages {

        stage("Pull") {
            steps {
                git credentialsId: 'sonar-token',
                    url: 'https://github.com/cloudmaster2025/sonar.git'
            }
        }

        stage("Build") {
            steps {
                sh '/opt/apache-maven-3.9.6/bin/mvn clean package'
            }
        }

        stage("Test") {
            steps {
                withSonarQubeEnv(credentialsId: 'my-sonar', installationName: 'my-sonar-1') {

                    sh '''
                    /opt/apache-maven-3.9.6/bin/mvn clean verify sonar:sonar \
                    -Dsonar.projectKey=My-Project
                    '''

                }
            }
        }

        stage("Quality-Gate") {
            steps {
                timeout(time: 60, unit: 'SECONDS') {
                    waitForQualityGate abortPipeline: true, credentialsId: 'my-sonar'
                }
            }
        }

        stage("Deploy") {
            steps {
                deploy adapters: [tomcat9(
                    alternativeDeploymentContext: '',
                    credentialsId: 'tom1',
                    path: '',
                    url: 'http://TOMCAT_SERVER:8080/'
                )],
                contextPath: 'student',
                war: 'target/*.war'
            }
        }
    }
}
