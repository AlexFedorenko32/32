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
                if exist build_dir (
                    dir build_dir
                ) else (
                    echo Директорія build_dir не існує
                )
                '''
            }
        }
        stage('Deploy') {
            steps {
                bat '''
                echo Запуск стейджа Deploy
                if exist build_dir (
                    rmdir /S /Q build_dir
                    echo Деплой завершено
                ) else (
                    echo Немає директорії для видалення
                )
                '''
            }
        }
    }
}
