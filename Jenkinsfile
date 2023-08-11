pipeline {
    agent any
    stages {
        stage('Clone'){
            steps {
                git 'https://github.com/NguyenVanDuc036/test_cicd.git'
            }
        }

        stage('Authenticate'){
            steps {
                sh "echo -n ${env.DOCKER_TOKEN} | docker login -u ${env.DOCKER_USER} --password-stdin"
            }
        }
    }
}