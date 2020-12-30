// SCRIPTED

// DECLARATIVE

pipeline {
	agent any
	// agent { docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	
	stages{
		stage('Build') {
			steps{
				sh 'docker version'
				sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
			}
		}	
		stage('Test') {
			steps{
				echo "Test"
			}
		}	
	}

}
