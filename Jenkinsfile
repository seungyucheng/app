pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building2..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing2..'
                sh 'exit 0'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying2....'
            }
        }
    }
}
