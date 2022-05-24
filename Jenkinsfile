pipeline {
    agent {
        docker{
            image 'android-container:sunflower'
            args '-u root'
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
