pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World from github'
            }
        }
        stage('Docker') {
            agent {
                docker {
                    image 'ubuntu'
                }
            }
            steps {
                echo 'Hello World from docker container'
                sh '''
                cat /etc/os-release
                '''
            }
        }
    }
}
