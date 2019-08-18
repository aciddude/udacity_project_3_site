pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                
                sh 'echo "Hello World - David Walton"'
                
                sh '''
                  echo "Multi-line works too!"
                  ls -lrtha
                '''
            }
        }
    }
}

