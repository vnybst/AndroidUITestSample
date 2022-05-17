pipeline {
    agent {
        docker {
        image 'bitriseio/docker-bitrise-base:latest'
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