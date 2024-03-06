pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "Jenkinsfile Build Stage"'
                build 'PES1UG21CS287-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "Jenkinsfile Test Stage"'
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "Jenkinsfile Deployment Stage"' 
                sh 'echo "deployed"'
            }
        }
    }
    post{
        failure{
            error 'Jenkinsfile Pipeline Failed'
        }
    }
}
