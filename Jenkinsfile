pipeline {
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh
                bat "docker-compose up -d selenoid selenoid-ui vnc_chrome:110.0"
            }
        }
		stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up selenium-docker"
            }
        }
        stage('Stop Grid') {
            steps {
                //sh
                bat "docker-compose down"
            }
        }
    }
}