node {
    stage('Checkout') {
        // Checkout code from the main branch of the Git repository
        git url: 'https://github.com/sikkumishra1993/Jenkins.git', branch: 'master'
    }

    stage('Build') {
        echo 'Building...'
        script {
            sh 'chmod +x build.sh'
            sh './build.sh'
        }
    }

    stage('Test') {
        echo 'Testing...'
        // Add your test commands here
    }

    stage('Deploy') {
        echo 'Deploying...'
        // Add your deploy commands here
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
