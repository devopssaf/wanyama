node {
  stage ('Clone Repository') {
  checkout scm
      }
  stage ('Build a Docker Image'){
  sh "docker build -t wanyama:1.0 ."
  }
  stage ('Deploy Docker Image'){
  sh "docker rm $(docker ps -a -q) -f"
  sh "docker container run --detach --publish 8088:80 --name first_web wanyama:1.0"
  }
  }
