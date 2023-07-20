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
    stage ('push artifact') {
        zip zipFile: '*', archive: false, dir: 'archive'
        archiveArtifacts artifacts: '*.zip', fingerprint: true
    }
}    