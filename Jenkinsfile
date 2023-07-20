node {
    stage('Take code from Git') { 
        git 'https://github.com/MariiaGalitsyna/jenkins_training.git'
    }
    stage('Results') {
        bat '''javac HelloWorld.java
               java HelloWorld'''
    }
    stage('store README') {
        archiveArtifacts artifacts: '*', onlyIfSuccessful: true
    }
    // stage('send email'){
    //     mail bcc: '', body: 'This is a test email', cc: '', from: '', replyTo: '', subject: 'Test Jenkins', to: 'mariia.galitsyna@gmail.com'
    // }
}    