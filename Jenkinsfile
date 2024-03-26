pipeline {
    agent any
    tools{
        maven '3.9.6'
    }
    stages {
        stage('Initialize'){
           steps{
                sh '''
                 echo "PATH = ${PATH}"
                 echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
        stage('Build'){
            steps{
                echo 'Hello world'
            }
        }
    }

}
