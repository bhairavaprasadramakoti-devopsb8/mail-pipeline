pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                error "Building the project"
            }
        }
    }
    post {
        always {
            script {
                def subject = "Job Status is: ${currentBuild.currentResult}"
                def body = "Build Number is ${currentBuild.number}\n" + "status is ${currentBuild.currentResult}\n" + "Job URL is ${env.BUILD_URL}"
                mail to: 'bhairavaprasadramakoti@gmail.com',subject: subject, body: body
            }
        }
    }
}
