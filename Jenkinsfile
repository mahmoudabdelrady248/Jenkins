pipeline {
    agent {
        label 'docker-agent-alpine'
    }

    triggers {
        pollSCM '* * * * *'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                sh '''
                cd myapp
                docker build -t mabdelrady/hello-world .
                '''
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run mabdelrady/hello-world'
            }
        }

        stage('Deliver') {
            steps {
                sh 'echo "Delivery steps here..."'
            }
        }
    }
}
