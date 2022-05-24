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
                bash '. /start.sh'
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
