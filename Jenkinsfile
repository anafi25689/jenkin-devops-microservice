pipeline {
    //agent any
	agent {docker {image 'maven:3.6.3'}}
    stages {

        stage ('Build') {
            steps {
				sh 'mv --version' // maven version
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
    }
    post {
        always {
            echo 'I Am Fine'
        }
        success {
            echo 'I ran because I was successful'
        }
        failure {  // تصحيح الكلمة هنا
            echo 'I ran because you failed'
        }
    }
}
