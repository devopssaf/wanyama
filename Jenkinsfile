node {
  stage ('Clone Repository') {
  checkout scm
      }
  stage ('Build a Docker Image'){
  sh "docker build -t wanyama:1.0 ."
  }
  stage ('Deploy Docker 2 Image'){
   sh "docker container run --detach --publish 8189:80 --name first_web_4 wanyama:1.0"
  }
  }
