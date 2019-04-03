node {
  stage ('Clone Repository') {
  checkout scm
      }
  stage ('Build a Docker Image'){
  sh "docker build -t wanyama:1.0 ."
  }
  stage ('Deploy Docker Image'){
   sh "docker container run --detach --publish 8089:80 --name first_web_3 wanyama:1.0"
  }
  }
