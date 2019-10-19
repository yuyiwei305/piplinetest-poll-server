pipeline {
    agent any
    environment {
        DOCKER_REPOSITORY_URL = "docker.io/visionyuyu"
        REMOTE_CODE_REPOSITORY_URL = "https://github.com/yuyiwei305/piplinetest-poll-server.git"
        REMOTE_HELM_CHART_REPOSITORY_URL = "https://git-codecommit.ap-northeast-1.amazonaws.com/v1/repos/rancher_catalog"
        GIT_TAG = sh(returnStdout: true, script: 'git rev-parse --short HEAD').trim()
  }
    stages {

        stage('Clone'){
            steps{
            withCredentials([usernamePassword(credentialsId: 'd7ab7df9-c005-487e-b1b7-918a812f55d5')]){
                sh """
                    git clone https://git-codecommit.ap-northeast-1.amazonaws.com/v1/repos/rancher_catalog 
                
                """
                }             
           }
       } 

  
        stage('Code Analysis') {    
            steps{
            echo "2.Helm test"
            sh "echo  $GIT_TAG"
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


