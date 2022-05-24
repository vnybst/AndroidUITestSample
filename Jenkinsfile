pipeline {
    agent {
        docker {
        image 'android-container:sunflower'
        args '-u root'
        sh 'chmod +x ./start.sh'
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
