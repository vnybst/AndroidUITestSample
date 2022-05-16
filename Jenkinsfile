pipeline {
    agent {
        docker { image 'registry.amarulasolutions.com:443/bitrise-android:latest' }
    }
    stages {
        stage('Build') {
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew assembleDebug'
            }
        }
    }
}