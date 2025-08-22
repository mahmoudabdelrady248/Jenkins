FROM jenkins/jenkins:2.516.1-jdk21

USER root

RUN apt-get update && apt-get install -y docker.io lsb-release ca-certificates curl && apt-get clean && rm -rf /var/lib/apt/lists/*

USER jenkins

RUN jenkins-plugin-cli --verbose --plugins "blueocean docker-workflow json-path-api"
