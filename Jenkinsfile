// CODE_CHANGES = getGitChanges()

pipeline {
    agent any
//     tools {
//         maven "Maven"
//     }
    
    parameters {
        string(name: "STRNAME", defaultValue: "", description: "string description")
        choice(name: "VERSION", choices: ['1.1.0', '1.2.0','1.3.0'], description: "")
        booleanParam(name: "executeTests", defaultValue: true, description: "")
    }
    
    environment {
        NEW_VERSION = "1.3.0"
        SERVER_CREDENTIALS = credentials("server-id")
    }
    
    
    
//     triggers {
//         pollSCM "* * * * *"
//         cron("0 0 * * *")
//     }
    
    stages {
        stage("Build") {
            when {
                expression {
                    params.executeTests == true
                }
                
//                 expression {
//                     BRANCH_NAME == "dev" && CODE_CHANGE == true
//                 }
            }
            
            steps {
                echo "build id: ${BUILD_ID}"
                echo "branch url: ${BRANCH_NAME}"
                script {
                    // i am able to use 'def' below because of the 'script' tag
                    def name = "somto"
                }
            }
        }
        
        stage("Deploy") {
            steps {
                sh "echo 'deploying...'"
                
// IF YOU DON;T WANT TO MAKE GLOBAL AS ABOVE
//                 withCredentials([usernameAndPassword(credentials: 'server-credentials', usernameVariable: USER, variable: PWD]) {
                    
//                 }
            }   
        }
    }
    
    post {
        always {
//             mail to: "vitusvictor41@gmail.com",
//                 subject: "done building",
//                 body: "body"
                emailext body: 'A Test EMail',
                        subject: 'Subject',
                        to: 'vitusvictor41@gmail.com onyibalusomto@outlook.com onyibalusomto@gmail.com',
                        mimeType: 'text/plain'
                
        }
                
    }
            
}
