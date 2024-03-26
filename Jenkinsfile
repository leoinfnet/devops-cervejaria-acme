pipeline {
    agent any
    tools{
        maven 'mvn'
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
        stage('Clean'){
            steps{
                sh 'mvn clean'
            }
        }
        stage('Package'){
                    steps{
                        sh 'mvn -DskipTests package'
                    }
                }
        stage('Copy'){
                    steps{
                        sh 'cp *.jar /tmp/jenkins/'
                    }
                }

    }

}
