pipeline {
    agent {
        label 'java-slave'
    }
    stages ('Build') {
        steps {
            echo "This is building the project"
        }
    }
    post {
        always {
            mail bcc: '', body: 'This is a test mail sent through pipeline', cc: '', from: '', replyTo: '', subject: 'Test Pipeline Mail', to: 'bhairavaprasadramakoti@gmail.com'
        }
    }
}
