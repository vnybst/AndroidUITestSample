pipeline {
    agent {
        docker{
            image 'android-container:sunflower'
            args '-u root --privileged'
        }
    }
    stages {
        stage('Build') {
            steps {
               sh 'chmod +x . /start.sh'
               sh '. /start.sh'
               sh './gradlew connectedAndroidTest'
            }
        }
    }
}
