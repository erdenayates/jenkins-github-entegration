pipeline {
    agent any
    stages {
        stage('Setting the variables values') {
            steps {
                sh '''#!/bin/bash
                 echo "hello world" 
                   '''
    }
}
        stage('Example') {
            steps {
                script {
                    echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                    ls -la
                    pwd
                }
                script {
            commit = sh(returnStdout: true, script: 'git log -1 --oneline').trim()

            String commitMsg = ""

            List commitMsgPre = commit.split(" ")

            for(int i=1; i<commitMsgPre.size(); i++){
            commitMsg += commitMsgPre.getAt(i) + " "}
            echo "Running ${commitMsg}"
            
                }
            }
            
        }
    }
}

