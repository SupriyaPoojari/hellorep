pipeline {
    agent any

    stages {
        stage('Fetch File') {
            steps {
                git 'https://github.com/SupriyaPoojari/hellorep.git'
            }
        }
        stage('Building'){
            steps{
               echo  'Building the project'
               bat 'javac Hello.java'
            }
        }
        stage('Executing'){
            steps{
                echo "Executing Progress"
                bat 'java Hello'
            }
        }
    }
    post{
        success{
            echo 'Pipeline Executed Successfully'
        }
        failure{
            echo "Pipeline Failed"
        }
    }
}
