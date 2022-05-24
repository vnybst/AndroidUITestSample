pipeline {
    agent {
        docker{
            'android-container:sunflower'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
