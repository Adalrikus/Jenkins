pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'gradle'
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
