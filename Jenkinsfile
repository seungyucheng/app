
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
                             disableSubmodules: false,
                             parentCredentials: true,
                             recursiveSubmodules: true,
                             reference: '',
                             trackingSubmodules: true]
                        ]
                ])
            }
        }

        stage('Extract') {
            steps {
                script {
                    props = readJSON file: 'config.json'
                    env.XCODE_VERSION = props.ios.xcode
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building2..'
                echo "XCODE_VERSION: ${env.XCODE_VERSION}"
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
