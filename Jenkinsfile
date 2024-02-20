pipeline {
    agent {
        label 'linux'
        }
                
    stages {
    
    /* The below stage is used to download the dependencies and check lint error in code. */ 
        stage('validating code') {
            steps {
                sh " echo validating code "
            }
        }

    /* The below stage is used to download the dependencies and build the code */ 
        stage('Building Nextjs') {
            steps {
                script {
                    if (env.gitlabTargetBranch=="master")
                        {
                        sh 'echo this is production branch'
                    }
                    else if (env.gitlabTargetBranch=="uat")
                        {
                        sh 'echo this is uat'
                    }
                    else if (env.gitlabTargetBranch=="development")
                        {
                        sh 'echo this is dev'
                    }    
                }
            }
        }

    }
}
