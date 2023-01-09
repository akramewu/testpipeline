
pipeline {
    agent any
    enviroment {
        NEW_VERSION = '1.5.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo "building version ${NEW_VERSION}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
                junit 'reports/**/*.xml'
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
