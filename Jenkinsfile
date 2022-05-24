pipeline {
    agent {
        docker {
        image 'android-container:sunflower'
        args '-u jenkins'
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
