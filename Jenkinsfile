pipeline {
    agent any
    environment {
        staging_server = "13.233.129.3" // Update the IP address to your server's IP
    }
    stages {
        stage('Deploy to Remote') {
            steps {
                script {
                    sh "scp -r ${WORKSPACE}/ root@${staging_server}:/var/www/html/info.php/"
                }
            }
        }
    }
}
