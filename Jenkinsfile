pipeline {
    agent {
        label 'aws-ec2'
    }

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
                sh 'python3 --version'
            }
        }

        stage('Run Code') {
            steps {
                echo 'Running hello.py ....'
                sh 'python3 hello.py'
            }
        }

        stage('Deliver') {
            steps {
                echo 'Deliver ....'
            }
        }
    }
}
