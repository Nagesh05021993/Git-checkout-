pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                git credentialsId: 'Password', url: 'https://github.com/kampatinagesh/test1.git'
            }
        }
        stage('ansible') {
            steps {
                ansiblePlaybook credentialsId: 'ansible_cred', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/nginx.yml', vaultTmpPath: ''
            }
        }
        
    }
}
