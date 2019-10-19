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
            withCredentials([usernamePassword(credentialsId: '2ffb4975-c0d8-4b0e-87cd-f17d96551a3a', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
    			sh """
    			    git clone https://yuyiwei-at-651538853910:eGoQeVrYyvF9mFg8fW1O2AbsWB2Wj%2bPv2%2fHGr9DlCU0%3d@git-codecommit.ap-northeast-1.amazonaws.com/v1/repos/rancher_catalog 

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


