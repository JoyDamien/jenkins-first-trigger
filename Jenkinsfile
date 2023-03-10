pipeline {
  agent any
    stages {
      stage('Jieyao Deng - Build Docker Image') {
        steps {
          bat "echo build-Docker-image"
          bat "docker image build -t myfirstimage:0.1 /cygdrive/c/Users/monsi/Downloads"
        }
      }
      stage('Jieyao Deng - Login to Dockerhub') {
        steps {
          bat "echo login-to-Dockerhub"
          bat "cat /cygdrive/c/Users/monsi/Downloads/Dockerhub_passwd.txt | docker login -u joydamien --password-stdin"
        }
      }
      stage('Jieyao Deng - Push image to Dockerhub') {
        steps{
          bat "echo push-image-to-Dockerhub"
          bat "docker image push joydamien/myfirstimage"
        }
      }
    }
}
