/* example of Jenkins doc: Using Docker with Pipeline
 * https://www.jenkins.io/doc/book/pipeline/do
 */
 
pipeline {
    agent {
        //docker { image 'rabbitmq:3.6.9-management' }
         docker {
           //label 'Agent'
           image 'rabbitmq:3.6.9-management'
           args  '--hostname linda-rabbit --name linda-rmq -p 15672:15672 -p 5672:5672'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo rabbitmq started'
            }
        }
    }
}
