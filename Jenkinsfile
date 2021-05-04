pipeline {
    agent any

    stages {
        stage('preparation') {
            steps {
                git 'https://github.com/hossamkhalil01/Booster_CI_CD_Project'
            }
        }
        stage('CI') {
            steps {
                sh 'docker build . -t hossam/django_cicd:1.0'
            }
        }
        stage('CD') {
            steps {
                sh 'docker run -d -p 8000:8000 hossam/django_cicd:1.0'
            }
        }
    }
}

