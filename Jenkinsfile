pipeline {
   agent any
   stages {
    stage('Deploy Web app to Azure'){
      when { changeset "app1/**"} //Will execute your steps if any file change inside the component_a directory
            steps {
                echo 'Hello World'
                sh '''ls -la
                echo "selaxxxm"
                echo "bla bla"'''
            }
    }

    stage('Deploy API service to Azure portal'){
        when { changeset "app2/**"} //Will execute your steps if any file change inside the component_b directory
            steps {
                echo 'Hello World'
                sh '''ls -la
                echo "selzzzzam"
                echo "bla bzzla"'''
            }
    }
}
}
