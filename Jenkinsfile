pipeline {
	agent any
	stages {
		stage ('build') {
			step {
				sh 'mvn clean package'
			}
			post {
				success {
					echo 'now archiving'
					archiveArtifacts artifacts: '**/target/*.war'
				}
			}
		}
		stage ('deploy to QA') {
			step {
				build job: 'Practice1-Deploy-QA'
			}
		}
	}
}
			
