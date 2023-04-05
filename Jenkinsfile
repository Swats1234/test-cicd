pipeline{
	agent any
	
	stages {
		stage('Build') {
			steps{
					git 'https://github.com/Swats1234/test-cicd.git'
					bat "mvn -Dmaven .test.failure.ignore=true clean package"
				}
			}
		stage('Test') {
			steps{
					git 'https://github.com/Swats1234/test-cicd.git'
					bat "mvn -Dmaven .test.failure.ignore=true clean test"
				}
			}
		stage('Deploy') {
			steps{
					git 'https://github.com/Swats1234/test-cicd.git'
					bat "mvn -Dmaven .test.failure.ignore=true clean deploy -DmuleDeploy"
					}
			}
		}
}
