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
               bat "mvn jar:jar install:install "
               bat "java -jar target/my-app-1.0-SNAPSHOT.jar"               
            }
        }
    }
}
