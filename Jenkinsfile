pipeline {
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh
                bat "docker-compose up -d selenoid seneloid-ui vnc_chrome"
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