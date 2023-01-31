pipeline {
    agent { label 'SPRING' }
    stages {
        stage('git_clone') {
            steps {
                git branch: 'main',
                       url: 'https://github.com/maheshryali123/jenkins_ansible.git'
            }
        }
        stage('ansible') {
            steps{
                 sh """
                 ansible-playbook -i hosts ansible.yaml -k
                 """
            }
        }
    }
}