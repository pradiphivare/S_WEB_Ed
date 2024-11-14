pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git 'https://github.com/ennded/EdTech-Website.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // If there are any dependencies (e.g., npm, yarn), install them
                echo 'No dependencies to install for static HTML, CSS, JS'
            }
        }

        stage('Test') {
            steps {
                // Optional: Run any JavaScript tests if applicable (if you have any)
                echo 'No tests configured for this static website'
            }
        }

        stage('Build') {
            steps {
                // No build steps needed for static websites
                echo 'No build steps needed for this static HTML/CSS/JS website'
            }
        }

        stage('Deploy') {
            steps {
                // Replace this with your actual deployment step, like S3 or FTP
                echo 'Deploying website...'
                // Example: For S3 Deployment
                // sh 'aws s3 sync . s3://your-s3-bucket --delete'

                // Example: For FTP Deployment
                // sh 'lftp -c "open -u username,password ftp://your-server.com; mirror -R ./ /path/to/deploy"'

                // Note: Set up your actual deployment commands here.
            }
        }
    }

    post {
        always {
            // Cleanup workspace after build
            cleanWs()
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs.'
        }
    }
}
