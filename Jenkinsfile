pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('Stage1') {
            steps {
                echo "Hello"
            }
        }
        stage('Stage2') { 
            steps {
                echo 'mvn test' 
            }
        stage('Stage3') { 
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
