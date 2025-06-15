pipeline {
    agent any
    stages {
        stage ('compilation') {
            steps {
                sh 'compile'
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
