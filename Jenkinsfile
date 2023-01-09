
pipeline {
    agent any
    tools{
        maven 'Maven 3.8.7'
        jdk 'jdk9'
    }
    environment {
        NEW_VERSION = '1.5.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo "building version ${NEW_VERSION}"
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application of Java version...'
                sh 'java -version'
            }
        }
        stage('Stage') {
            steps {
                echo 'Staging of the Java version for deployment....'
            }
        }
        stage('Deploy to QA') {
            steps {
                echo 'Deploying the Java version to Dev environment....'
            }
        }
    }
}
