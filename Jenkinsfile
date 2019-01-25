pipeline {
environment {
        JAVA_HOME = tool('java')
    }
  agent any
  stages {
    
    stage('Deploy CloudHub') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        sh 'echo ${ANYPOINT_CREDENTIALS_PSW} ${ANYPOINT_CREDENTIALS_PSW}'
  
        sh '/usr/maven/apache-maven-3.3.9/bin/mvn clean package mule:deploy -X -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}' 
        
         
      }
    }
  }
}