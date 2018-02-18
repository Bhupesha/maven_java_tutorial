pipeline {
    agent { label 'test' }
    tools {
        git 'git'
        
    }
    stages {
        stage('Example Build') {
            steps {
                sh 'git --help'
            }
        }
    }
}
