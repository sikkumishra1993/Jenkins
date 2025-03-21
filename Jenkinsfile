pipeline {
    agent { label 'first-jenkins' }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                 script {
                    sh './build.sh'
                }
                // Add your build commands here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy commands here
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
