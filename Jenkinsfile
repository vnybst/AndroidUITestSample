pipeline {
    agent {
        docker{
            image 'android-container:sunflower'
            args '-u root --privileged -v $HOME/.m2:/home/jenkins/.m2 -ti -u 496'
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
