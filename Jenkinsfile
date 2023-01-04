pipeline {
    agent any 
    
    tools {
        maven 'Maven3'
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/RutujaPawal/test1']]])
            }
        }      
        stage ('Build') {
            steps {
                sh 'mvn clean install'           
            }
        }   
    }
}
