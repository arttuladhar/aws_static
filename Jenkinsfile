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
        stage('Upload to AWS'){
            steps {
                withAWS(credentials:'aws-static') {
                // do something
                    s3Upload(file:'index.html', bucket:"art-udacity-static-web")
                }
            }
        }
    }
}
