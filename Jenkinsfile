pipeline {
	agent {label "multibranch"}
	options {
		buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
		disableConcurrentBuilds()
	
	}
	stages {
		stage('Hello') {
			steps {
				echo "hello"
			}
		}
		stage('Only fix branches') {
			when {
				branch "fix-*"
			}
			steps {
				echo "I do things in fix branches"
			}
		}
	}
}
