pipeline {
	//agent any
	agent { 
		docker { image 'maven:3.8.5'} 
	}
	environment {
		dockerHome = tool 'Docker'
		mavenHome = tool 'Maven3.8.5'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker --version'
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Teste'){
			steps{
				echo "Integration Test"
			}
		}
	}
	post {
		always{
			echo 'Im Awesome. I run always'
		}
		success{
			echo 'I run when you are successful'
		}
		failure{
			echo 'I run when you fail'
		}
	}
}
