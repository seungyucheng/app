pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building4..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing4..'
                sh 'exit 0'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying4....'
            }
        }
    }
    
    post {
        always {
            archiveArtifacts artifacts: 'Jenkinsfile', fingerprint: true
        }
    }
}
