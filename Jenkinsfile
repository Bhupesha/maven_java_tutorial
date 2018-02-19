pipeline {
    agent { label 'test' 
           parameters {
            choice(
                name: 'Nodes',
                choices:"Linux\nMac",
                description: "Choose Node!")
            choice(
                name: 'Versions',
                choices:"3.4\n4.4",
                description: "Build for which version?" )
            string(
                name: 'Path',
                defaultValue:"/home/pencillr/builds/",
                description: "Where to put the build!")
         
          }
           
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
                    sh 'cd NumberGenerator && mvn install'
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

