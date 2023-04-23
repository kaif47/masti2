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
        stage('Clone') {
            steps {
                bat 'git clone "https://github.com/kaif47/masti2.git"'
            }
        }
        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }
        stage('Test') {
            steps {
                echo "Testing the project..."
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the project..."
                bat 'xcopy C:/Users/Kaif Bijali/masti2 "C:/xampp/htdocs"'
            }
        }
    }
}
