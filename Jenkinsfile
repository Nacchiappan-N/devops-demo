pipeline {
    agent any
    //tools {
        //maven 'Maven'
    //}

    stages {

        stage('Build Maven') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'GIT_REPO', url: 'https://github.com/devopshint/jenkins-nexus.git']]])

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }   
   
    }
}
