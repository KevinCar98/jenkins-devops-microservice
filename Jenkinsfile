pipeline {
	agent { 
		docker { image 'maven:3.8.5'} 
	}
	stages {
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Build"

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
