pipeline {
    agent any 
    stages {
        stage('Build') {
            when {
                branch "master"
            }
            steps {
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
