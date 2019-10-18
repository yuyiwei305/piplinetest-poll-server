pipeline {
  agent any
  environment {
        DOCKER_REPOSITORY_URL = "pollserver"
        REMOTE_CODE_REPOSITORY_URL = "https://github.com/yuyiwei305/piplinetest-poll-server.git"
  }
  stages {
    stage('Clone') {
      echo "1.Clone stage"
    }
  stages {
    stage('Code Analysis') {
      echo "2.Code Analysis Stage"
    }
  stages {
    stage('Build Image') {
      echo "3.Build Docker Image Stage"
    }
  stage('Push Image') {
    steps {
      echo "4.Push Docker Image Stage"  
    }
  stage('Pudh helm chart') {
      echo "5.Push Docker Image Stage"  
    }
}