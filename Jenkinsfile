pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                echo 'display maven'
                "sh 'export PATH=$MAVEN_HOME:$PATH && mvn clean package' "
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
