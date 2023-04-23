pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], 
                doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
                userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/kaif47/masti2.git']]])
            }
        }
        stage('Build') {
            steps {
                bat 'echo "Building the project..."'
                bat 'dir'
            }
        }
        stage('Test') {
            steps {
                bat 'echo "Testing the project..."'
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo "Deploying the project..."'
                bat 'xcopy /s * "C:/xampp/htdocs/"'
            }
        }
    }
}
