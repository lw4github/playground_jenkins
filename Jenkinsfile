/* example of Jenkins doc: Using Docker with Pipeline
 * https://www.jenkins.io/doc/book/pipeline/do
 */
 
pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
