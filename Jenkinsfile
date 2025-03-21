node {
    def branch = 'main'

    stage('Checkout') {
        // Checkout code from the main branch of the Git repository
        git url: 'https://github.com/sikkumishra1993/Jenkins.git', branch: branch
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
    echo 'Cleaning up...'
    cleanWs()
    if (currentBuild.result == 'SUCCESS') {
        echo 'Build succeeded!'
    } else {
        echo 'Build failed!'
    }
}
