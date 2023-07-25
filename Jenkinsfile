// node {
//     stage('Take code from Git') { 
//         git 'https://github.com/MariiaGalitsyna/jenkins_training.git'
//     }
//     stage('Results') {
//         bat '''javac HelloWorld.java
//                java HelloWorld'''
//     }
//     stage('store README') {
//         archiveArtifacts artifacts: '*', onlyIfSuccessful: true
//     }
//     // stage('send email'){
//     //     mail bcc: '', body: 'This is a test email', cc: '', from: '', replyTo: '', subject: 'Test Jenkins', to: 'mariia.galitsyna@gmail.com'
//     // }
// }    
pipeline {
    // agent { docker { image 'maven:3.9.3-eclipse-temurin-11' } }
    agent any
    stages {
        stage('build') {
            steps {
                bat 'set'
                bat 'echo Command executed'
                bat '''javac HelloWorld.java
                       java HelloWorld'''
            }
        }
    }
    post {
        always{
            echo "This will always run"
            archiveArtifacts artifacts: '*', fingerprint: true
        }
        success{
            echo "This will run only if successful"
        }
        failure{
            echo "This will run only if failure"
        }
    }
}