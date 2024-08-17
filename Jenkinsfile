pipeline {
    agent any
    stages {

        stage ('Build') {
            steps {
                echo "Build"
            }
        }

        stage ('Test') {
            steps {
                echo "Test"
            }
        }

        stage ('Integration Test') {
            steps {
                echo "Integration Test"
            }
        }
    } post {
		always {
			echo 'I Am Fine'
		}
		success {
			echo 'I run will I was successfull'
		}
		faliure {
			echo 'I run will you fail'
		}
	}
}
