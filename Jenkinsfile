pipeline {
    agent any
    environment {
        DOCKER_REPOSITORY_URL = "docker.io/visionyuyu"
        REMOTE_CODE_REPOSITORY_URL = "https://github.com/yuyiwei305/piplinetest-poll-server.git"
        REMOTE_HELM_CHART_REPOSITORY_URL = "git-codecommit.ap-northeast-1.amazonaws.com/v1/repos/rancher_catalog"
        REMOTE_HELM_CHART_REPOSITORY_GITHUB_URL="github.com/yuyiwei305/bookinfo-demo"
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
            withCredentials([usernamePassword(credentialsId: 'ba4dfb37-b290-488b-946f-23b165c20f69', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
    			sh """
    			    git clone https://${GIT_USERNAME}:${GIT_PASSWORD}@${REMOTE_HELM_CHART_REPOSITORY_URL}

    			    ls

    			    pwd

    			   """
				}
            }   
       }
  
        stage('Build Image') {
            steps{
            echo "3.Build Docker Image Stage"
            sh """
               pwd

               """
            }   
        }

        stage('Push Image') {
            steps {
            echo "4.Push Docker Image Stage" 
            sh """
               pwd

               """ 
            }
        }
  
        stage('Pudh helm chart') {
            steps {
            echo "5.Push Docker Image Stage"
            sh """
               pwd

               """  
            } 
        }
    }
}


