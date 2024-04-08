pipeline {
	agent {  label 'Linux-Node' }
	stages {
		stage('---clean----'){
			tools {
				maven 'maven_3.9.6'
			}
			steps {
				sh 'mvn --version'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'maven_3.9.0'
			}
			steps {
				sh 'mvn --version'
				sh "mvn test"
			}
		}
		
	}
	post {
		success {
			echo 'job was built successfully'
		}
		failure {
			echo 'job was not build..it was failed'
		}
	}
}
