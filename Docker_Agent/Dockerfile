FROM jenkins/agent:jdk17

USER root

RUN apt-get update && apt-get install -y docker.io lsb-release ca-certificates curl && apt-get clean && rm -rf /var/lib/apt/lists/*
