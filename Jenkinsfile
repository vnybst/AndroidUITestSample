pipeline {
    agent {
        docker {
        image 'android-container:sunflower'
        args '--privileged -v $HOME/.m2:/home/jenkins/.m2 -ti -u 496'
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
