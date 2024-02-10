//DECLARATIVE

pipeline {
	agent any
	// agent { docker { image 'maven:latest'} }
	stages {
		stage('Build') {
			steps {
				// sh 'mvn --version'
				echo "$path"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
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