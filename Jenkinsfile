pipeline {
    agent any
    tools { 
        maven 'MAVEN354' 
        jdk 'JDK181' 
    }
    stages {
        stage ('Initialize') {
            steps {
                   bat "echo %path%"
            }
        }

        stage ('Build') {
 				steps {
               bat "mvn install" 
            }
        }
    }
}
