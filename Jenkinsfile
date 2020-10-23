pipeline {

    agent any

    stages {
        
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
