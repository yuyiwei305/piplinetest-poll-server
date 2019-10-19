pipeline {
    agent any
    environment {
        DOCKER_REPOSITORY_URL = "pollserver"
        REMOTE_CODE_REPOSITORY_URL = "https://github.com/yuyiwei305/piplinetest-poll-server.git"
  }
    stages {

        stage('Clone'){
            steps{
            echo "1.Clone stage"
            }
       } 

  
        stage('Code Analysis') {    
            steps{
            helm version --client
            }   
       }
  
        stage('Build Image') {
            steps{
            echo "3.Build Docker Image Stage"
            }   
        }

        stage('Push Image') {
            steps {
            echo "4.Push Docker Image Stage"  
            }
        }
  
        stage('Pudh helm chart') {
            steps {
            echo "5.Push Docker Image Stage"  
            } 
        }
    }
}


