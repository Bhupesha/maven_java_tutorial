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
    
    stage ('Build') {
            steps {
                    sh 'cd NumberGenerator & mvn install'
                    powershell '''
                               $list = Get-childitem
                               foreach($file in $list)
                               {
                                 Write-Output("$file")
                               }
                    '''           
                   /* powershell 'Write-Output "Hello, World!"' */
            }
    
    }
    }
    
}

