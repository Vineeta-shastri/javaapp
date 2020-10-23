pipeline {

    agent any

    tools
    {
      gradle 'gradle_settings'
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

      stage('Compile') {
            steps {
                gradlew('clean', 'classes')
            }
        }
}
}
