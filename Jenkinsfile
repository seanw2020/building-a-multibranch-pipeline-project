pipeline {
    agent any
    parameters {
      string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo ${params.Greeting} World!'
            }
        }
        stage('Test') {
            steps {
                sh 'echo test'
            }
        }
    }
}
