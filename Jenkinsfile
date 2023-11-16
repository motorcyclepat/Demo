pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'apt-get update' 
            }
        }
        stage('Test'){
            steps {
                sh 'apt-get upgrade'
            }
        }
        stage('Deploy') {
            steps {
                sh 'apt-get autoremove' 
            }
        }
    }
}
