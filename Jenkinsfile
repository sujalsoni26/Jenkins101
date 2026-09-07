pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building ....'
            }
        }

        stage('Check Python') {
            steps {
                bat 'python --version'
            }
        }

        stage('Run Code') {
            steps {
                echo 'Running hello.py ....'
                bat 'python hello.py'
            }
        }

        stage('Deliver') {
            steps {
                echo 'Deliver ....'
            }
        }
    }
}
