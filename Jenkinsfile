pipeline {
    agent {label 'Dev-slave'}
    tools {
        maven 'Maven3.1.1'
        jdk 'java_home'
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
                    powershell '''
                               $list = Get-childitem
                               foreach($file in $list)
                               {
                                 Write-Output("$file")
                               }
                    '''           
                   /* powershell 'Write-Output "Hello, World!"' */
            }
            
            
             /* post {
                success {
                    junit 'target/surefire-reports/*.xml'
                        }
                 } */
               

           
            }
        }
    
}
