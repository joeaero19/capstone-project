pipeline {
	 agent {label 'ec2-slave'}

	triggers {
		pollSCM 'H/2 * * * *'
	}

	options {
		disableConcurrentBuilds()
		buildDiscarder(logRotator(numToKeepStr: '14'))
	}

	stages {
		stage("Build Package") {
			
			steps {
				sh 'cd complete && ./mvnw package'
				//sh 'test/run.sh'
			}
		}

	}

	
}
