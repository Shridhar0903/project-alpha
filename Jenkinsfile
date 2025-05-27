pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Shridhar0903/project-alpha'
            }
        }
        stage('Build ') {
            steps {
                  bat 'javac simple.java'
            }
        }
        stage('test') {
            steps {

                bat 'java simple'
           
            }
        }
        stage('Deploy') {
            steps {
                scripts{
                    echo " Java program run successfully"
                }
            }
        }
    }
  triggers{
     pollSCM('H/5 * * * *')
  }
}


  
