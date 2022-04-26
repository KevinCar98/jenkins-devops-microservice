pipeline {
	agent any

	stages {
		stage('Build'){
			steps{
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
	} post{
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
