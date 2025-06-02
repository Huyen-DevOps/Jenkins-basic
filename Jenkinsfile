pipeline {
    agent any

    stages {
        stage('Giai đoạn 1: In ra Hello') {
            steps {
                echo 'Xin chào! Đây là bước đầu tiên của bạn với Jenkins Pipeline.'
            }
        }

        stage('Giai đoạn 2: In ngày giờ') {
            steps {
                script {
                    def now = new Date().format("yyyy-MM-dd HH:mm:ss", TimeZone.getTimeZone('UTC'))
                    echo "Thời gian hiện tại (UTC): ${now}"
                }
            }
        }

        stage('Giai đoạn 3: Mô phỏng build') {
            steps {
                echo 'Đang "build" ứng dụng giả lập...'
                sh 'sleep 2'
                echo 'Hoàn tất mô phỏng build.'
            }
        }
    }

    post {
        success {
            echo '🎉 Pipeline đã chạy thành công!'
        }
        failure {
            echo '❌ Pipeline thất bại. Kiểm tra lại các bước.'
        }
    }
}
