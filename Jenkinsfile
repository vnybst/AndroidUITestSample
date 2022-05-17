pipeline {
    agent {
        docker {
        image 'registry.amarulasolutions.com:443/bitrise-android:365'
        args '--privileged -v $HOME/.m2:/home/jenkins/.m2 -ti -u 496'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh '/Users/vinaybisht/emulator.sh'
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}