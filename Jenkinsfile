pipeline {
    agent any
    tools {
        maven 'Maven3.1.1'
        jdk 'java8'
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = %PATH%"
                    echo "M2_HOME = %M2_HOME%"
                '''
            }
        }

        stage ('Build') {
            steps {
                    bat 'cd NumberGenerator & mvn install'
            }
            
            stage ('execute powershell Script) {
                   steps {
                        powershell 'Write-Output "Hello, World!"'
                   }
             /* post {
                success {
                    junit 'target/surefire-reports/*.xml'
                        }
                 } */
               
           
            }
        }
    
}
