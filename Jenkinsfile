pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git url: "https://github.com/moncaris/jenkins-scm.git", branch: 'main'
            }
        }
        
        stage('Run Hello World') {
            steps {
                // Run the Python script
                script {
                    sh 'python3 hello.py'
                }
            }
        }
    }
    
    post {
        always {
            // Archive the results or any logs if needed
            echo 'Pipeline finished'
        }
    }
}

