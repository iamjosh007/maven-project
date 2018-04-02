pipeline {
    agent any

    tools {
	maven 'MAVEN_HOME'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
	stage ('Deploy to Staging'){
	    steps {
		build job: 'deploy-to-staging'
	    }
	}
    }
}
