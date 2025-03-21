pipeline {
    agent any
    parameters {
        string(name: 'PARAM1', defaultValue: 'default_value', description: 'Enter a string parameter')
        booleanParam(name: 'FLAG', defaultValue: true, description: 'Select a boolean flag')
        choice(name: 'CHOICE', choices: ['Option1', 'Option2', 'Option3'], description: 'Select an option')
    }
    stages {
        stage('build') {
            steps {
                echo "Building with PARAM1: ${params.PARAM1}"
                echo "FLAG is set to: ${params.FLAG}"
                echo "Selected CHOICE: ${params.CHOICE}"
                // Add your build steps here
            }
        }
        stage('test') {
            steps {
                echo 'Testing...'
                // Add your test steps here
            }
        }
        stage('deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy steps here
            }
        }
    }
    post {
        always {
            echo 'Cleaning up...'
            cleanWs()
        }
        success {
            echo 'Success'
        }
        failure {
            echo 'Failed'
        }
    }
}
