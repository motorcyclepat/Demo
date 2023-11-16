pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'touch .file' 
            }
        }
        stage('Test'){
            steps {
                sh 'echo "this success" > .file'
                sh 'echo "additional text" >> .file'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cat .file' 
            }
        }
    }
}
