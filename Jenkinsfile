pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project'
                writeFile file: 'output.txt',
                          text: 'Jenkins build successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'output.txt'
            echo 'Build completed successfully'
        }
    }
}