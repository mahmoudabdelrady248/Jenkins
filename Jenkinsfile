pipeline {
    agent {
        label 'docker-agent-python'
    }

    triggers {
        pollSCM '* * * * *'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                sh '''
                cd myapp
                docker ps -a
                docker build -t mabdelrady/hello-world .
                '''
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker run --rm mabdelrady/hello-world
                docker ps -a
                '''
            }
        }

        stage('Deliver') {
            steps {
                sh 'echo "Delivery steps here..."'
            }
        }
    }
}
