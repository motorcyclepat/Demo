pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Vet candidate') {
            steps {
                sh 'echo $Parameter_Name'
            }
        }
        stage('Document'){
            steps {
                sh 'echo "Here is where we begin documentation with Jira and SNOW"'
            }
        }
        stage('Build and Deploy'){
            steps {
                sh 'echo "Here is where we perform actual build and deploy"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "here is where we validate our build is running via predefined responses or health checks"' 
            }
        }
        stage('report'){
            steps {
                sh 'echo "here is where we report various metrics to accountable individuals and manage ticket closure "'
            }
        }
    }
}
