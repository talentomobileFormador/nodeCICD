pipeline {
    agent any
    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -t ${name-app} ."
                }
                script {
                    sh "docker tag ${name-app} formadorfullstacktalentomobile/nodecicd:${BUILD_NUMBER}"
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push formadorfullstacktalentomobile/nodecicd:${BUILD_NUMBER}"
                }
            }
        }
    }
}