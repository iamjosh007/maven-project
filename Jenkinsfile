pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                echo 'display maven'
                /usr/bin/sh 'mvn -version'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
