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
                mvn "-Dmaven.test.failure.ignore=true install "
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
