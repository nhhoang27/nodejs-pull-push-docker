pipeline{
    agent { label 'linux'}

    stages {
        stage('gitclone') {
            steps {
                git 'https://github.com/nhhoang27/nodejs-pull-push-docker.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t 172.16.10.109/nodeapp_test:latest .'
            }
        }

        stage('Push') {
            steps {
                sh 'docker push 172.16.10.109/nodeapp_test:latest'
            }
        }
    }
} 