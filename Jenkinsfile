pipeline {
    agent any
    tools{
        maven 'maven_3.9.2'
    }
    stages{
        stage('Build Maven'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Thatsha/Thatsha-DevOps-Automation']]])
                sh 'mvn clean install'
            }
        }
       
    }
}
