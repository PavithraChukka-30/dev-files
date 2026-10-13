pipeline {
    agent any
    stages {
        stage('Ansible fetch') {
            steps {
                sh 'ansible-playbook deploy.yml'
            }
        }
        stage('Show files') {
            steps {
                sh 'ls -l files'
                archiveArtifacts artifacts: 'files/*.txt', fingerprint: true
            }
        }
    }
}
