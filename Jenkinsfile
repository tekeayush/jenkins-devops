//DECLARATIVE

pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	post{
		always {
			echo "I Run Withoud Any condition"
		}
		success {
			echo "I Run When Code Ran Succesfully"
		}
		faillure {
			echo "I Run When Code Failed"
		}
	}
}