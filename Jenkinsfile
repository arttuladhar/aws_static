pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World!"'
                sh '''
                echo "Yay Multiline Shell Scripting"
                ls -lah
                '''
            }
        }
    }
}
