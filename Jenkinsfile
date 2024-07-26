import java.time.Instant

stage('test') {
	node {
		emailext body: 'Jenkins CI Email test' + Instant.now(),
				subject: 'Jenkins CI Email test' + Instant.now(),
				to: 'yrodiere@redhat.com'
		emailext body: 'Jenkins CI Email test' + Instant.now(),
				subject: 'Jenkins CI Email test' + Instant.now(),
				to: 'yoann@hibernate.org'
		emailext body: 'Jenkins CI Email test' + Instant.now(),
				subject: 'Jenkins CI Email test' + Instant.now(),
				to: 'y.rodiere@gmail.com'
	}
}
