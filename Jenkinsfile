pipeline {
    agent {
        docker{
            'android-container:sunflower'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh './start.sh'
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
