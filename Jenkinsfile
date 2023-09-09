pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/Neelabai/jenkins-nexus.git']]])
            }
        }

        stage('Build') {
            steps {
                // Build the Maven project
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests, if applicable
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your project, if needed
                // You can add deployment steps here
            }
        }
    }

    post {
        always {
            // Cleanup or perform other post-build actions
        }
    }
}

       
