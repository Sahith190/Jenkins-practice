pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                    ls -ltr
                    pwd
                    echo "Hello from Github push webhook event"

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
            }
        }
    }
    post { 
        always { 
            echo 'I always run whether the job is success or not'
        }
        success {
            echo 'I will run only when job is success'
        }
        failure {
            echo 'i will run when failure'
        }
    }
}
