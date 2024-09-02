
/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout([$class: 'GitSCM',
                        branches: [[name: "*/${BRANCH_NAME}"]], // Replace with your branch
                        userRemoteConfigs: [
                                [
                                    url: 'https://github.com/seungyucheng/app.git',
                                    credentialsId: 'seungyu'
                                ]
                            ],
                        extensions: [
                            [$class: 'SubmoduleOption',
                             recursiveSubmodules: true,
                             reference: '',
                             trackingSubmodules: true]
                        ]
                ])
            }
        }

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
