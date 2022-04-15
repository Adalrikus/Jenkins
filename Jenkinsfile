pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                gradle wrapper --gradle-version 7.4.2
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
