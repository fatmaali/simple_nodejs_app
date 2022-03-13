pipeline {
    agent any

    stages {
        stage('Getting Repo Files') {
            steps {
                git branch: "${GIT_BRANCH}", credentialsId: 'git_hub_token', url: 'https://github.com/ahmedKhaled1995/simple_nodejs_app.git'
            }
        }
        
        stage('Building Code') {
            steps {
                sh "docker build -t mynodeapp:v1.0 ."
            }
        }
    }
}
