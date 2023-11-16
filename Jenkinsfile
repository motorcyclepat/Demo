pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'whoami' 
            }
        }
        stage('Test'){
            steps {
                sh 'sudo -l'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo $GROUP' 
            }
        }
    }
}
