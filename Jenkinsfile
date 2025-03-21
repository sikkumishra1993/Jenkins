pipeline
{
agent { label 'master' }
parameters {
        string(name: 'PARAM1', defaultValue: 'default_value', description: 'Enter a string parameter')
        booleanParam(name: 'FLAG', defaultValue: true, description: 'Select a boolean flag')
        choice(name: 'CHOICE', choices: ['Option1', 'Option2', 'Option3'], description: 'Select an option')
    }
stages{

    stage('build'){
        steps{
            echo 'Building project'
        }
    }
    stage('test'){
        steps{
            echo 'Testing project'
        }
    }
    stage('deploy'){
        steps{
            echo 'Deploying project'
        }
    }
}

post{

    always{

        echo 'cleaning up'
        cleanWs()
    }
    success{
        echo "Success"
    }
    failure{
        echo "Failure"
    }
}

}
