pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                echo 'Prepare'
            }
        }
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Log') {
            steps {
                sh 'echo "build finished" > build.log'
            }
        }
    }
    post {
        always {
            echo "无论任务构建成功与否执行此代码块"
        }
        success {
            echo "任务构建成功执行此代码块"
        }
        failure {
            echo "任务构建失败执行此代码块"
        }
    }
}
