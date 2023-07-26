pipeline {
    // agent { docker { image 'maven:3.9.3-eclipse-temurin-11' } }
    agent any
    stages {
        stage('build') {
            steps {
                bat 'set'
                bat 'echo Command executed'
            }
        }
    }
    post {
        always{
            echo "This will always run"
            // archiveArtifacts artifacts: '*', fingerprint: true
        }
        success{
            echo "This will run only if successful"
        }
        failure{
            echo "This will run only if failure"
        }
    }
}