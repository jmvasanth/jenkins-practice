pipeline {
    agent { node { label 'AGENT-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                ls -lrt
                pwd
                echo "Hello from GitHub Push Webhook Events"
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // error ' This is failed'
            }
        }
    }

    post {
        always {
            echo ' I will always run whether job is success or not'
        }
        success{
            echo ' I will run only when job is success'
        }
        failure{
            echo ' I will run when failure'
        }
    }
}