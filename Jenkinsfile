pipeline {
    agent any
    stages {
        stage('docker build') {
            steps {
                sh "docker ps"
                sh "docker pull node:16"
                sh "docker build -t ${name-app} ."
                sh "docker tag ${name-app} formadorfullstacktalentomobile/nodecicd:${BUILD_NUMBER}"
            }
        }
        stage('docker push') {
            steps {
                sh "docker push formadorfullstacktalentomobile/nodecicd:${BUILD_NUMBER}"
            }
        }
    }
}