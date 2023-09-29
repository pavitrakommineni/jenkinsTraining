pipeline {
stages {
  stage('SCM code') {
   steps {
    git 'https://github.com/hellokaton/java11-examples.git'
   }
  }
 stage('Build') {
  steps {
   sh 'mvn clean package'
  }
 }
 stage('Publish') {
  steps {
  // Add steps to publish artifacts or deploy the application
  // For example, you can use the 'archiveArtifacts' step to archive built artifacts
  archiveArtifacts 'target/*.jar'
emailext body: '''Hi Pavitra,

This is a test notification from jenkins''', subject: 'Jenkins Test Notification', to: 'pavitra17.kommineni@gmail.com
     }
  } 
}
}
