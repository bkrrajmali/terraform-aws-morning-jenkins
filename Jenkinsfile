pipeline {
    agent any 
    stages {
        stage('Checkout from Git') { 
            steps {
                git branch: 'prod' , url: 'https://github.com/bkrrajmali/terraform-aws-morning-jenkins.git'
            }
        }
        stage('Terraform Init') { 
            steps {
                script {
                    sh 'terraform --version'
                }
            }
        }
        stage('Terraform validate') { 
            steps {
                script {
                    sh 'terraform validate'
                }
            }
        }
    }
}