pipeline {
    agent any
    
    triggers {
        echo "polling ..."
        pollSCM "* * * * *"
    }
    
    stages {
        stage("Build") {
            steps {
                echo "building... "
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
