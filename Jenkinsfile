//DECLARATIVE

pipeline {
	// agent any
	agent { docker { image 'maven:latest'} }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
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
		failure {
			echo "I Run When Code Failed"
		}
	}
}