pipeline{
    agent any 
    stages {
        stage('clone'){
            steps{
                git 'https://github.com/LongNgo436/test.git'
            }
	stage('docker'){
            steps{
                withDockerRegistry(credentialsId: 'docker-long', url: 'https://index.docker.io/v1/') {
		    sh 'docker build -t longngo7122/getting-started .'
		    sh 'docker push longngo7122/getting-started '
		}
            }
        }
    }
}
