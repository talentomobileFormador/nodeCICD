pipeline {
    agent any
    stages {
        stage('docker build') {
            steps {
                sh "docker ps"
                sh "docker pull node:16"
                sh "docker build -t pruebacicd ."
                sh "docker tag pruebacicd formadorfullstacktalentomobile/nodecicd:${BUILD_NUMBER}"
            }
        }
        stage('docker push') {
            steps {
                sh "docker push formadorfullstacktalentomobile/nodecicd:${BUILD_NUMBER}"
            }
        }
    }
}