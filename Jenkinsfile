pipeline {
    agent any
    stages {
	    stage('Pull Latest Image') {
            steps {
                //sh
                bat "docker pull ramociocea/selenium-docker:latest"
            }
        }
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
    }
	post{
		always{
			//archiveArtifacts artifacts: 'Reports/**'
			bat "docker-compose down"
		}
	}
}