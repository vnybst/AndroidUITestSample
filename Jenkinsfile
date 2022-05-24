pipeline {
    agent {
        docker.image( 'android-container:sunflower').withRun('-u root').inside{
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
