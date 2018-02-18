pipeline {
    agent { label 'test' }
    tools {
        maven 'Maven3.1.1'
        jdk 'java8'
    }
    stages {
        stage('Example Build') {
            steps {
                sh 'git --help'
            }
        }
    }
}
