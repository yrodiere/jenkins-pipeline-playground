pipeline {
	agent {
		docker {
			image 'maven:3.8.1-adoptopenjdk-11'
			args '-v /var/run/docker.sock:/var/run/docker.sock --group-add 1002'
		}
	}
	stages {
		stage('Example Build') {
			steps {
				sh 'ls -l /var/run/docker.sock'
				sh 'echo $UID $GID'
				sh 'cat /etc/passwd'
				sh 'cat /etc/group'
				sh 'mvn docker:start'
				sh 'mvn docker:stop'
			}
		}
	}
}
