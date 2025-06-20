pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/Vijaya150/static-website.git'
            }
        }

        stage('Deploy to S3') {
            steps {
                sh '''
                  aws s3 sync . s3://myhtmlbucketvg
                '''
            }
        }
    }
}
