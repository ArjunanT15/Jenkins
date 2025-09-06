pipeline {
    agent {
        docker { image 'node:16-alpine' }
    }

    stages {
        stage('Hello World') {
            steps {
                sh 'echo "console.log(\\"Hello, World!\\")" > app.js'
                sh 'node app.js'
            }
        }

        stage('Check NPM') {
            steps {
                sh 'npm -v'
            }
        }
    }
}
