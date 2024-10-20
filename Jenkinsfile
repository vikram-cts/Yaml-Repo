pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                // Clones the repository from GitHub
                git branch: 'main', url: 'https://github.com/sirinali07/Yaml-Repo.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                // Runs the specified Ansible playbook
                ansiblePlaybook playbook: 'playbooks/Install-apache2.yaml',
                                inventory: 'hosts/inventory.ini',
                                credentialsId: 'ansible-ssh-key'
            }
        }
    }
}