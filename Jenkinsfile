pipeline {
    agent any
    tools { 
        maven 'MAVEN354' 
        jdk 'JDK181' 
    }
    stages {
        stage ('Initialize') {
            steps {
                   echo "%path%"
            }
        }

        stage ('Build') {
 				steps {
               bat "mvn clean compile" 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
