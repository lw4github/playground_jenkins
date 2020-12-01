/* example of Jenkins doc: Using Docker with Pipeline
 * https://www.jenkins.io/doc/book/pipeline/do
 */
 
pipeline {
    agent {
        docker { image 'rabbitmq:3.6.9-management' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo rabbitmq started'
            }
        }
    }
}
