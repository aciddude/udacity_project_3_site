pipeline {
    agent any
    stages {
        stage ('SayHello') {
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
                    s3Upload(bucket:"udacity-project-3-site", path:'/', includePathPattern:'**/*', workingDir:'dist', excludePathPattern:'**/Jenkinsfile')
                }

            }
        } 
    }
}

