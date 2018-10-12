pipeline {
    agent any
    tools { 
        maven 'MAVEN354' 
        jdk 'JDK181' 
    }
    stages {
        stage ('Initialize') {
            steps {
                    echo %path%
            }
        }

        stage ('Build') {
            steps {
                echo 'This is a minimal pipeline.'
            }
        }
    }
}
