pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Nithishkumar0064/new-java-project.git'
            }
        }

        stage('Email-notification') {
            steps {
                 emailext attachLog: true, body: '''Hi
                 please find job details as bellow  

                 Job: ${JOB_NAME} - Build # ${BUILD_NUMBER}
                 URL: ${BUILD_URL}

                 Thank you
                 Nithishkumar
                ''', subject: 'Details about jenkins jobs', to: 'nithilak.2014@gmail.com'

            }
        }
    }
}
