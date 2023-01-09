
pipeline {
    agent any
    tools{
        maven 'Maven'
    }
    environment {
        NEW_VERSION = '1.5.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo "building version ${NEW_VERSION}"
                sh "mvn install"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
            }
        }
        stage('Stage') {
            steps {
                echo 'Staging of the application for deployment....'
            }
        }
        stage('Deploy to QA') {
            steps {
                echo 'Deploying the application to QA environment....'
            }
        }
    }
}
