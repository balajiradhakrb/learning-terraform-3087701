pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                 script{
                        dir("terraform")
                        {
                            git "https://github.com/balajiradhakrb/learning-terraform-3087701.git"
                        }
                    }
                }
            }
        stage('init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Deploy') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
