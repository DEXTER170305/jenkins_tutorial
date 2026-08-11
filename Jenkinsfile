```groovy
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Compiling application...'
                bat 'node --version'
                bat 'node index.js'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                bat 'node index.js'
            }
        }

        stage('Package') {
            steps {
                echo 'Creating build package...'
                bat 'echo Build executed on %date% %time% > build-info.txt'
            }
        }
    }

    post {
        success {
            echo 'Build successful! Ready for release.'
        }

        failure {
            echo 'Build failed!'
        }
    }
}
```
