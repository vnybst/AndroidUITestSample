pipeline {
    agent {
        docker {
        image 'android-container:sunflower'
        args '-u root'
        }
    }
    stages {
        stage('Build') {
            steps {
                bash -c './start.sh'
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
