pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Shridhar0903/project-alpha'
            }
        }
        stage('Build') {
            steps {
                bat 'javac simple.java'
            }
        }
        stage('Test') {
            steps {
                bat 'java simple'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo "Java program ran successfully"
                }
            }
        }
    }
    triggers {
        pollSCM('H/5 * * * *')
    }
}
