pipeline {
    agent any 
    
    tools {
        maven 'maven'
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/yogesh2188/MavenRepo.git']])
            }
        }      
        stage ('Build') {
            steps {
                sh 'mvn clean install'           
            }
        }   
    }
}
