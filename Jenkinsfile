node {
  stage ('Clone Repository') {
  checkout scm
      }
 stage ('Removee Docker Image'){
sh "docker rm 715176f26799 -f"
}
  stage ('Build a Docker Image'){
  sh "docker build -t wanyama:1.0 ."
  }
  stage ('Deploy Docker Image'){
   sh "docker container run --detach --publish 8089:80 --name first_web_2 wanyama:1.0"
  }
  }
