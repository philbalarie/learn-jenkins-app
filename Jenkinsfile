pipeline {
     agent any

    stages {
        stage('Docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                    npm ci
                    npm run build
                '''
            }
        }
    }
}
