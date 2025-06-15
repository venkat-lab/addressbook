pipeline {
    agent any
    tools { 
      maven 'maven3.9.6' 
      jdk 'JAVA_HOME' 
    }
    stages {
        stage ('compilation') {
            steps {
                sh 'mvn -B compile'
            }
        }
        stage ('test') {
            steps {
                sh 'mvn -B test'
            }
        }
        stage ('integration test') {
            steps {
                sh 'mvn -B verify'
            }
        }   

        stage ('package') {
            steps {
                sh 'mvn -B package'
            }
        }
 
    }
}
