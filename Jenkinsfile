pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                gradle 'wrapper'
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
