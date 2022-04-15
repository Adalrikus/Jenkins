pipeline {
    agent any
    tools {
        gradle 'Gradle-7.4.2'
    }
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
