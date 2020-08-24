pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('Build') {
            steps {
                echo "Hello"
            }
        }
        stage('Test') { 
            steps {
                echo 'mvn test' 
            }
        stage('Clean') { 
            steps {
                sh 'mvn clean' 
            }
            post {
                always {
                    echo 'mvn test'
                }
            }
        }
    }
}
