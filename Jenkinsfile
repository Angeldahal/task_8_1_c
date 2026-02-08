pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Task: Compile and package the application into a build artifact.'
        echo 'Tool: Maven'
      }
    }

    stage('Unit and Integration Tests') {
      steps {
        echo 'Task: Run unit tests and integration tests to validate functionality and component interaction.'
        echo 'Tools: JUnit, Testcontainers'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Task: Perform static code quality analysis to enforce standards and detect bugs/code smells.'
        echo 'Tool: SonarQube (Jenkins SonarQube Scanner)'
      }
    }

    stage('Security Scan') {
      steps {
        echo 'Task: Scan dependencies and code to identify known vulnerabilities.'
        echo 'Tool: OWASP Dependency-Check'
      }
    }

    stage('Deploy to Staging') {
      steps {
        echo 'Task: Deploy the application to a staging server.'
        echo 'Tool: AWS CodeDeploy (AWS EC2 staging)'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Task: Run integration/end-to-end tests on staging to validate production-like behaviour.'
        echo 'Tool: Postman/Newman'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Task: Deploy the validated release to a production server.'
        echo 'Tool: AWS CodeDeploy (AWS EC2 production)'
      }
    }
  }
}

