pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM',
        //         branches: [[name: '*/main']],
        //         userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']]])
        //     }
        // }

        stage('Build') {
            steps {
                build 'PES1UG22CS5156'
                sh 'g++ PES1UG22CS156.cpp -o PES1UG22CS156-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22CS156-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error "Pipeline failed"
        }
    }
}
