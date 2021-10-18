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
		stage("test: baseline (jdk8)") {
			
			steps {
				sh 'test/run1.sh'
			}
		}

	}

	
}
