pipeline { 
	agent any

	environment {
		MAJOR_VERSION=1.00
	}
	stages {
		stage('build') {
			steps {
				sh 'ant -f build.xml -v'
			}
		}
	}


	post {
		always {
			archieveArtifacts artifacts: 'dist/*.jar',fingerprint: true
		}
	}
}