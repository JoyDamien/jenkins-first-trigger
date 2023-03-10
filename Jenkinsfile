pipeline {
  agent any
    stages {
      stage('Jieyao Deng - Build Docker Image') {
        steps {
          sh "echo build-Docker-image"
          sh "docker image build -t myfirstimage:0.1 /cygdrive/c/Users/monsi/Downloads"
        }
      }
      stage('Jieyao Deng - Login to Dockerhub') {
        steps {
          sh "echo login-to-Dockerhub"
          sh "cat /cygdrive/c/Users/monsi/Downloads/Dockerhub_passwd.txt | docker login -u joydamien --password-stdin"
        }
      }
      stage('Jieyao Deng - Push image to Dockerhub') {
        steps{
          sh "echo push-image-to-Dockerhub"
          sh "docker image push joydamien/myfirstimage"
        }
      }
    }
}
