pipeline {
    agent any
    tools{
        maven '3.9.6'
    }
    stages {
        stage('Initialize'){
            sh '''
             echo "PATH = ${PATH}"
             echo "M2_HOME = ${M2_HOME}"
            '''
        }
        stage('Build'){
            steps{
                echo 'Hello world'
            }
        }
    }

}
