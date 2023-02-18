pipeline {
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh
                bat "docker-compose up -d selenoid selenoid-ui test-chrome"
            }
        }
		stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up test-framework"
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