pipeline {
    agent any

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run test stage?')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building version..."
            }
        }

        stage('Test') {
            when {
                expression { return params.executeTests }
            }
            steps {
                echo "Running tests..."
            }
        }
    }
}
