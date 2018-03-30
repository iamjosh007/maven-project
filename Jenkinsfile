pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                echo 'display maven'
                sh 'mvn -version'
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
