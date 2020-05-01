pipeline {
    agent any
    stages {
        stage('Lint HTML'){
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS'){
            steps {
                withAWS(credentials:'aws-static') {
                // do something
                    s3Upload(bucket:"art-udacity-static-web", workingDir:'dist', includePathPattern:'**/*');
                }
            }
        }
    }
}
