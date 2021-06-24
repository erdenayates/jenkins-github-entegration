pipeline {
    agent any
    stages {

        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                script {
            commit = sh(returnStdout: true, script: 'git log -1 --oneline').trim()

            String commitMsg = ""

            List commitMsgPre = commit.split(" ")

            for(int i=1; i<commitMsgPre.size(); i++){
            commitMsg += commitMsgPre.getAt(i) + " "}
            echo "${commitMsg}"
            
                }
            }
            
        }
        stage('Setting the variables values') {
            steps {
            sh '''#!/bin/bash
                 ls -la
                 cd ${commitMsg}/ 
               '''
    }
}
    }
}

