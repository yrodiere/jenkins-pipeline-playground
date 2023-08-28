stage('test') {
	node( 'Worker' ) {
		stage('test-nested1') {
			checkout scm
			sh "echo -n 'user.name: '; git config 'user.name' || echo 'None'"
			sh "echo -n 'user.email: '; git config 'user.email' || echo 'None'"
		}
		stage('test-nested2') {
			sh "touch foo"
			sh "git add -A"
			sh "git commit -m 'foo'"
			sh "git log"
			sh "env"
		}
	}
}
