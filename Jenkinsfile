pipeline {
    agent {
        docker { image 'registry.amarulasolutions.com:443/bitrise-android:365' }
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew assembleDebug'
            }
        }
    }
}