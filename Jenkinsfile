stage('Configure') {
	node( 'Worker&&Containers' ) {
		docker.image('quay.io/hibernate/awestruct-build-env:latest').inside('--pull always') {
			configFileProvider([configFile(fileId: 'release.config.ssh', targetLocation: '/home/dev/.ssh/config')]) {
				sshagent(['hibernate-ci.frs.sourceforge.net']) {
					sh "ssh frs.sourceforge.net echo SUCCESS"
				}
			}
		}
	}
}
