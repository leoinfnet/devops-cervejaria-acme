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
                        sh 'cp /var/jenkins_home/workspace/cervejaria-acme/target/cervejaria-acme-0.0.1-SNAPSHOT.jar /tmp/jenkins/cervejaria-acme-0.0.1-SNAPSHOT.jar'
                    }
                }

    }

}
