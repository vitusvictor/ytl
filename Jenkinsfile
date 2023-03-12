pipeline {
    agent any
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
