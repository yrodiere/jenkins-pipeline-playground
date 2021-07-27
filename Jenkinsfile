stage('test') {
	node( 'Worker&&Containers' ) {
		checkout scm
		sh "docker info"
		sh "docker login"
		sh "docker info"
	}
}
