pipeline {
    agent any
    stages {
        stage ('Say Hello - Build init') {
            steps {
                
                sh 'echo "Hello World - David Walton"'
                
                sh '''
                  echo "Multi-line works too!"
                  ls -lrtha
                '''
            }
        }
        stage ('Upload to AWS') {
            steps {
                
                withAWS(credentials:'jenkins-pipeline-aws') {
                    // do something
                    s3Upload(bucket:"udacity-project-3-site", file:'index.html')
                }
            }
        } 
    }
}

