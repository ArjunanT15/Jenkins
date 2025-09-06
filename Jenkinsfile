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
          stage('Say Hello') {
            steps {
                sh 'echo "Hello from Jenkins & Node.js!"'
                sh 'node -v'
                sh 'npm -v'
            }
        }
    }
}
