pipeline {
    agent any

    stages {
    //     stage('Checkout') {
    //         steps {
    //             // Get code from a GitHub repository
    //             git 'https://github.com/your-username/your-repo.git'
    //         }
    //     }
        
        stage('Build') {
            steps {
                // Run the maven build
                script {
                    echo ${everything}
            }
        }
        
        stage('Test') {
            steps {
                // Run the maven test
                echo "test"//sh 'mvn test'
            }
            post {
                always {
                    // Archive the test results
                    echo "post" //junit '**/target/surefire-reports/TEST-*.xml'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy the application (this is a placeholder command)
                sh 'echo "Deploying the application..."'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
