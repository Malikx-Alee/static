pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(credentials:'aws-static') {
					s3Upload(file:'index.html', bucket:'udacity-static-jenkins', path:'path/to/target/index.html')
				}
				sh 'echo "Hello World"'
				sh '''
					echo "Multiline shell steps works too"
					ls -lah
				'''
			}
		}
	}
}