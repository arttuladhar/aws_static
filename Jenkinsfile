pipeline {
    agent any
    stages {
        stage('Hello World') {
            steps {
                sh 'echo "Hello World!"'
                sh '''
                echo "Yay Multiline Shell Scripting"
                ls -lah
                '''
            }
        }
        stage('Lint HTML'){
            steps {
                sh 'tidy -q -e *.html'
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
