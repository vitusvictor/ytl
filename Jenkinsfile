pipeline {
    agent any
    
    triggers {
        pollSCM "* * * * *"
    }
    
    stages {
        stage("Build") {
            steps {
                echo "build id: ${BUILD_ID}"
            }
        }
        
        stage("Deploy") {
            steps {
                sh "echo 'deploying...'"
            }   
        }
    }
}
