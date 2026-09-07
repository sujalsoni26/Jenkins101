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
