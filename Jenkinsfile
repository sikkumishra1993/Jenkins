node {
    def branch = env.BRANCH_NAME

    stage('Checkout') {
        // Checkout code from Git repository
        git url: 'https://github.com/sikkumishra1993/Jenkins.git', branch: main
    }

    stage('Build') {
        steps {
            echo 'Building...'
            script {
                sh 'chmod +x build.sh'
                sh './build.sh'
            }
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

    // Post-build actions
    post {
        always {
            echo 'Cleaning up...'
            cleanWs()
        }
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
