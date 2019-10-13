pipeline {
    agent any {
      parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
      }
      docker {
            image 'node:6-alpine'
            rgs '-p 3000:3000 -p 5000:5000'
      }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
