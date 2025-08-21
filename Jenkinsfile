pipeline {
    agent {
        label 'docker-agent-python'
    }

    triggers {
        pollSCM '* * * * *'
    }

    stages {
        stage('Debug docker in agent') {
            steps {
                sh '''
                echo "DOCKER_HOST=$DOCKER_HOST"

                echo "Inspect agent container"
                docker inspect $HOSTNAME
                '''
            }
        }

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
                sh '''
                docker run --rm mabdelrady/hello-world
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
