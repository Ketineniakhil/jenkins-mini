pipeline{
	//agent any
	agent {docker {image 'maven:3.6.3'} }
	stages{
		stage('Build'){
			steps{
				sh 'mv --version'
				echo "build"
			}
		}
		stage('Test'){
			steps{
				echo "test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "test in"
			}
		}
	} 
}
