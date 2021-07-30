stage('Configure') {
	node( 'Worker&&Containers' ) {
		docker.image('quay.io/hibernate/awestruct-build-env:latest').inside('--pull always') {
			def jdkPath = tool(name: 'OpenJDK 11 Latest', type: 'jdk')
			echo "$jdkPath"
			sh "ls $jdkPath"
			sh "$jdkPath/bin/java --version"
			sh "java --version"
		}
	}
}
