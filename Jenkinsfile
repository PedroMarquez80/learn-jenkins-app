pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:19-alpine'
                    reuseNpde true
                }
            }
            steps {
                sh ''' 
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}