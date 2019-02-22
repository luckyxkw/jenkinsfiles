pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
		sh 'echo "hello world"'
		retry(3) {
			sh './fake.sh'
		}
                sh 'mvn --version'
            }
        }
    }
}
