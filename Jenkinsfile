pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo Hello, Windows!'
            }
        }
        stage('Test') {
            steps {
                bat '''
                echo Запуск стейджа Test
                dir build_dir
                '''
            }
        }
        stage('Deploy') {
            steps {
                bat '''
                echo Запуск стейджа Deploy
                rmdir /S /Q build_dir
                echo Деплой завершено
                '''
            }
        }
    }
}
