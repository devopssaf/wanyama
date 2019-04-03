node {
  stage ('Clone Repository') {
  checkout scm
      }
  stage ('Build a Docker Image'){
  sh "docker build -t wanyama:1.0 ."
  }
  stage ('Deploy Docker Image'){
  sh "docker container run --detach --publish 8088:80 --name first_web devopssaf/wanyama:1.0"
  }
  stage ('Push Image to Docker Hub'){
  sh "docker login -u 'devopssaf' -p 'Safar1com' "
  sh "docker tag wanyama:1.0 devopssaf/wanyama:1.0"
  sh "docker push devopssaf/wanyama:1.0"
  }
  }
