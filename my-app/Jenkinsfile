pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Saiteja13081/jenkins-app.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh '''
                pkill node || true
                nohup node app.js &
                '''
            }
        }
    }
}
