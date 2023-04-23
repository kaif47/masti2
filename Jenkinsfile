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
                sh 'echo "Building the project..."'
                sh 'ls -la'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing the project..."'
            }
        }
    }
}
