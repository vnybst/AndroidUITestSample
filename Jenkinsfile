pipeline {
    agent {
        docker{
            image 'android-container:sunflower'
            args '-u root'
            sh './start.sh'
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
