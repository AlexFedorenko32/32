pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo Hello, Windows!'
            }
        }
    }
}
        stage('Test') {
            steps {
                sh '''
                echo "Запуск стейджа Test"
                ls -la build_dir
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                echo "Запуск стейджа Deploy"
                rm -rf build_dir
                echo "Деплой завершено"
                '''
            }
        }
    }
}
