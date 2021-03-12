pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo "TEST BUILD STAGE"
                //sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh './scripts/jenkins/test.sh'
            }
        }
    }
}