pipeline {  
    agent {
        label 'Ansible-Node'
    }
    stages {
        stage('Clone') {
            steps {
               git 'https://github.com/oadin1/maven-web-app.git'
            }
        }
        stage('Build') {
            steps {
               sh 'mvn clean package'
            }
        }
        stage('Create Image'){
            steps{
               steps {
                	script {
                		sh 'ansible-playbook task.yml'
                	}
                }
            }
    }
}
