pipeline {
    agent any
    environment {
        dockerHome = tool 'myDocker'    // تأكد من أن هذا الإسم يطابق ما تم تعريفه في Jenkins Global Tool Configuration
        mavenHome = tool 'myMaven'      // تأكد من أن هذا الإسم يطابق ما تم تعريفه في Jenkins Global Tool Configuration
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${PATH}"  // تأكد من إضافة `:` بين المسارات
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'   // عرض إصدار Maven
                sh 'docker version' // عرض إصدار Docker
                echo "Build"
            }
        }

        stage('Test') {
            steps {
                echo "Test"
            }
        }

        stage('Integration Test') {
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
        failure {
            echo 'I ran because you failed'
        }
    }
}
