pipeline {
    agent any

    parameters {
        string(name: 'ref', defaultValue: 'refs/heads/main', description: 'Branch reference')
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Branch reference: ${params.ref}"
                    echo "Branch reference: ${params.P_REF}"
                    echo "Branch reference: ${params.P_AUTHOR}"
                }
            }
        }
    }
}

// properties ([
//     parameters([
//         string(name: 'P_REF'),
//         string(name: 'P_AUTHOR')
//     ])
// ])

// pipeline {
//     agent any

//     stages {
//     //     stage('Checkout') {
//     //         steps {
//     //             // Get code from a GitHub repository
//     //             git 'https://github.com/your-username/your-repo.git'
//     //         }
//     //     }
        
//         stage('Build') {
//             steps {
//                 // Run the maven build
//                 script {
//                     echo "Branch: ${P_REF}"
//                     echo "Author: ${P_AUTHOR}"
//                 }
//             }
//         }
        
//         stage('Test') {
//             steps {
//                 // Run the maven test
//                 echo "test"//sh 'mvn test'
//             }
//             post {
//                 always {
//                     // Archive the test results
//                     echo "post" //junit '**/target/surefire-reports/TEST-*.xml'
//                 }
//             }
//         }
        
//         stage('Deploy') {
//             steps {
//                 // Deploy the application (this is a placeholder command)
//                 sh 'echo "Deploying the application..."'
//             }
//         }
//     }
    
//     post {
//         success {
//             echo 'Pipeline succeeded!'
//         }
//         failure {
//             echo 'Pipeline failed!'
//         }
//     }
// }
