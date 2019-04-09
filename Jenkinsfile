pipeline {
    agent any 
    stages {
        stage('Build') {
            when {
                branch "master"
            }
            steps {
                sh './gradlew build'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
