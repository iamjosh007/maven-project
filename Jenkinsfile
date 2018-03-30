pipeline {
    agent any
        tools {
           MAVEN_HOME '/opt/apache-maven-3.5.2'
        }
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
