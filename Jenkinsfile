// This is the file that Jenkins will execute, typically named 'Jenkinsfile'

pipeline {
    // Defines where the pipeline will run. 'any' means Jenkins will pick an available agent.
    agent any

    // Defines the steps of the continuous delivery process
    stages {
        // --- Stage 1: Build ---
        stage('Build') {
            steps {
                echo 'Starting application build...'
                // Placeholder command: Compiles the Factorial.java file (if it were in the workspace)
                // If you were running a real Maven/Gradle project, this would be 'sh "mvn clean install"'
                echo 'Build successful.' 
            }
        }

        // --- NEW STAGE: Static Analysis ---
        stage('Static Analysis') {
            steps {
                echo 'Running static code analysis (e.g., SonarQube scan)...'
                // In a real pipeline, this would run tools like SonarScanner or Checkstyle.
                echo 'Code quality check passed.'
            }
        }

        // --- Stage 2: Test ---
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                // Placeholder command: Runs the Java program
                // If you were running real tests, this would be 'sh "mvn test"'
                echo 'Tests passed successfully.'
            }
        }

        // --- Stage 3: Deploy ---
        stage('Deploy') {
            steps {
                echo 'Deploying application to staging server...'
                // Placeholder command: Deploys the application
                echo 'Deployment complete.'
            }
        }
    }

    // --- Post-build Actions ---
    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'SUCCESS: The pipeline ran without errors.'
        }
        failure {
            echo 'FAILURE: Check the logs for errors.'
        }
    }
}
