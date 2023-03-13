// CODE_CHANGES = getGitChanges()

pipeline {
    agent any
    environment {
        NEW_VERSION = "1.3.0"
        SERVER_CREDENTIALS = credentials("server-id")
    }
    
    
    
    triggers {
//         pollSCM "* * * * *"
        cron("0 0 * * *")
    }
    
    stages {
        stage("Build") {
//             when {
//                 expression {
//                     BRANCH_NAME == "dev" && CODE_CHANGE == true
//                 }
//             }
            
            steps {
                echo "build id: ${BUILD_ID}"
                echo "branch url: ${BRANCH_NAME}"
            }
        }
        
        stage("Deploy") {
            steps {
                sh "echo 'deploying...'"
            }   
        }
    }
}
