pipeline {
    agent any


    stages {
       stage('Build') {
          steps {
             sh 'gradle clean compileJava'
             sh './gradlew clean build'
          }
       }
       stage('Deploy'){
                  steps{
                      sh 'cf push gateway-app -p ./build/libs/gateway-application-0.0.1-SNAPSHOT.jar'
                  }
       }
    }
}
