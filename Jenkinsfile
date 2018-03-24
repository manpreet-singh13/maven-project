pipeline {
	agent any
	stages{
		stage('Build'){
			steps {
				sh 'mvn package clean'
			}
			post {
				success {
					echo 'Now Archiving...'
					archiveArtifacts artifacts: '**/target/*.war'
				}
			}
		}
	}
}
		
	
