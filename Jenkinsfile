 pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                echo "Запуск стейджа Build"
                mkdir build_dir
                echo "Hello Jenkins!" > build_dir/output.txt
                cat build_dir/output.txt
                '''
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
