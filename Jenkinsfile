pipeline {
    agent any
    environment {
        DOCKER_REPOSITORY_URL = "docker.io/visionyuyu"
        REMOTE_CODE_REPOSITORY_URL = "https://github.com/yuyiwei305/piplinetest-poll-server.git"
        REMOTE_HELM_CHART_REPOSITORY_URL = "git-codecommit.ap-northeast-1.amazonaws.com/v1/repos/rancher_catalog"
        GIT_TAG = sh(returnStdout: true, script: 'git rev-parse --short HEAD').trim()
  }
    stages {

        stage('Clone'){
            steps{
            echo "clone 1111"            
            }
       } 

  
        stage('Code Analysis') {    
            steps{
            withCredentials([usernamePassword(credentialsId: 'd7ab7df9-c005-487e-b1b7-918a812f55d5', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
    			sh """
    			    git push https://${GIT_USERNAME}:${GIT_PASSWORD}@${REMOTE_HELM_CHART_REPOSITORY_URL}

    			   """
				}
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


