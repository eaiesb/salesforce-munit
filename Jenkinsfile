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
        sh '/usr/maven/apache-maven-3.3.9/bin/mvn deploy -P cloudhub -Dmule.version=3.9.1 -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}'
         
      }
    }
  }
}