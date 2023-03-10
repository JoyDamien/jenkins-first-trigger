pipeline {
  agent any

  stages {
    stage('Jieyao Deng - Build Docker Image') {
      steps {
	echo "Here we build a Docker image."
	docker image build -t="my_first_image" .
      }
    }
    stage('Jieyao Deng - Login to Dockerhub') {
      steps {
	echo "Here we login to Dockerhub."
	cat C:\Users\monsi\Downloads\Dockerhub_passwd.txt | docker login -u joydamien --password-stdin
      }
    }
    stage('Jieyao Deng - Push image to Dockerhub') {
      steps{
        echo "Here we push image to Dockerhub."
	docker image push joydamien/my_first_image
      }
    }
  }
}
