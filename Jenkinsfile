//DECLARATIVE

pipeline {
	agent any
	environment {
		dockerHome = tool 'dev-ayush-docker'
		mavenHome = tool 'dev-ayush'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	// agent { docker { image 'maven:latest'} }


	stages {
		stage('CheckOut') {
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "$path"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
			}
		}
		stage('compile') {
			steps {
				sh 'mvn clean clean compile'
			}
		}
		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}
		stage('Integration Test') {
			steps {
				sh 'mvn failsafe:integration-test failsafe:verify'
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