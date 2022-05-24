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
                chmod +x 'start.sh'
                ./start.sh
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
