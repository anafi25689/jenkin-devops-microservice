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
        echo 'I ran because I was successful'
    	}
    	ذfailure {  // تم تصحيح الكلمة هنا
        echo 'I ran because you failed'
    	}
}

}
