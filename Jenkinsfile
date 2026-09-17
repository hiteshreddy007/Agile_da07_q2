pipeline {
    agent any
    
    parameters {
        choice(
            name: 'ENVIRONMENT', 
            choices: ['dev', 'staging', 'prod'], 
            description: 'Select the target environment to build the Student Management System:'
        )
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com<your-github-username>/student-management-system.git'
            }
        }
        
        stage('Show Parameter') {
            steps {
                echo "Selected Target Environment for Student System: ${params.ENVIRONMENT}"
            }
        }
        
        stage('Build for Environment') {
            steps {
                echo "Building the Student Management and Academic Performance System for the ${params.ENVIRONMENT} environment..."
            }
        }
    }
}
