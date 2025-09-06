pipeline {
    agent none   // disable global agent

    stages {
        stage('Hello World with Node') {
            agent {
                docker { image 'node:16-alpine' }
            }
            steps {
                // Hello World using Node
                sh 'echo "console.log(\\"Hello, World from Node.js!\\")" > app.js'
                sh 'node app.js'
            }
        }

        stage('Install NPM Package') {
            agent {
                docker { image 'node:16-alpine' }
            }
            steps {
                sh 'npm init -y'        // create package.json
                sh 'npm install lodash' // install a sample package
            }
        }

        stage('Verify Node & NPM') {
            agent {
                docker { image 'node:16-alpine' }
            }
            steps {
                sh 'node --version'
                sh 'npm --version'
            }
        }
    }
}
