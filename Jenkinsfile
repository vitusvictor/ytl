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
                echo ${BUILD_ID}
            }
        }
        
        stage("Deploy") {
            steps {
                sh "echo 'deploying...'"
            }   
        }
    }
}
