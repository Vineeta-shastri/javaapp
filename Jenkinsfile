pipeline {

    agent any

    tools
    {
      gradle 'gradle v6.7'
    }

    stages {
       stage('Cleanup Workspace') {
                  steps {
                      cleanWs()
                      bat ' echo done '
                  }
              }
        
      stage('Code Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: 'master']], 
                    userRemoteConfigs: [[url: 'https://github.com/Vineeta-shastri/javaapp.git']]
                ])
            }
        }


}
}
