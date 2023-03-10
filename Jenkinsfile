pipeline {
  agent any
    stages {
      stage('Jieyao Deng - Build Docker Image') {
        steps {
          bat "echo build-Docker-image"
          bat "docker image build -t my-first-image ."
        }
      }
      stage('Jieyao Deng - Login to Dockerhub') {
        steps {
          bat "echo login-to-Dockerhub"
          bat "type Dockerhub_passwd.txt | docker login -u joydamien --password-stdin"
        }
      }
      stage('Jieyao Deng - Push image to Dockerhub') {
        steps{
          bat "echo push-image-to-Dockerhub"
	  bat "docker tag my-first-image joydamien/my-first-image"
          bat "docker image push joydamien/my-first-image"
        }
      }
    }
}
