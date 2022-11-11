# ansible-config-mgt
Devops: The new world order!
inventory of tools needed.
Inventing new tools for automation...
Re-inventing the the world of IT!

Sample Jenkinsfile
==============

pipeline {
    agent any

  stages {
    stage('Initial cleanup') {
      steps {
        dir("${WORKSPACE}") {
          deleteDir() 
        }
      }
    }
    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }
    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }
     stage('Package') {
       steps {
         script{
          sh 'echo "Packaging Stage"'
        }
      }
    }
     stage('Deploy') {
      steps {
        script {
          sh 'echo "Deploying to Dev"'
        }
      }
    }
    stage("Clean Up") {
      steps {
        cleanWs()
        }
    }
  }
}