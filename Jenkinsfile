pipeline {
    agent any

    environment{
        AWS_DEFAULT_REGION = 'eu-north-1'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Vijaya150/static-website.git'
            }
        }

        stage('Deploy to S3') {
            steps {
                sh '''
                  aws s3 sync . s3://staticbucketvg-git-pipeline
                '''
            }
        }
    }
}
