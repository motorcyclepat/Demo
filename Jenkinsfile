https://github.com/motorcyclepat/Demo/pipeline {
    agent any

    parameters {
        string(name: 'ENVIRONMENT', description: 'Select environment', defaultValue: 'dev')
        reactiveChoice(name: 'BRANCH', description: 'Select branch', script: """
            // Use the selected environment to dynamically generate the branch options
            def branchOptions = ['dev': 'development', 'qa': 'qa', 'prod': 'master']
            return branchOptions[params.ENVIRONMENT]
        """)
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the selected branch
                    checkout([$class: 'GitSCM', branches: [[name: "*/${params.BRANCH}"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], url: 'https://github.com/motorcyclepat/Demo/']]])
                }
            }
        }

        stage('Build') {
            steps {
                // Your build steps here
                echo "Building the project..."
            }
        }

        // Add more stages as needed

    }
}
