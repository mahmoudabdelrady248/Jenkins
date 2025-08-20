# docker network create jenkins

# docker run --name jenkins-docker -d --privileged --network jenkins -v jenkins-data:/var/jenkins_home -e DOCKER_TLS_CERTDIR= docker:dind

# cd Docker_Agent

# docker build . -t myjenkins-blueocean:2.516.1-1

# docker run --name jenkins-blueocean -d --user root --network jenkins -p 8080:8080 -v jenkins-data:/var/jenkins_home -e DOCKER_HOST=tcp://docker:2375 --restart=on-failure myjenkins-blueocean:2.516.1-1
