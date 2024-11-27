pipeline {
    agent any 
    stages {
        stage('Checkout from Git') { 
            steps {
                git branch: 'prod' , url: 'https://github.com/bkrrajmali/terraform-aws-morning-jenkins.git'
            }
        }
        stage('Terraform version') { 
            steps {
                script {
                    sh 'terraform --version'
                }
            }
        }
        stage('Terraform init') { 
            steps {
                script {
                    sh 'terraform init'
                }
            }
        }
    }
}