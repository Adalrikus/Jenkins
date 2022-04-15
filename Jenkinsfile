pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'gradle wrapper'
                sh './gradlew check'
            }
        }
    }
    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
}
