pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                 git branch: 'master', credentialsId: '1f67fa8c-8308-4936-8430-14f8d3810415', url: 'https://github.com/Mujeeb78/project_chat_application/'
            }
        }
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}

