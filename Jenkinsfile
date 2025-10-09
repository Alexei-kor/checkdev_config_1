pipeline {
    agent any
    stages {
        stage('compile') {
            steps {
                bat 'mvn.cmd compile'
            }
        }
         stage('test') {
            steps {
                bat 'mvn.cmd test'
            }
        }
        stage('package') {
            steps {
                bat 'mvn.cmd package'
            }
        }
    }
    post {
        success {
            echo 'Сборка прошла успешно!'
        }
        failure {
            echo 'Сборка завершилась неудачно.'
        }
    }
}