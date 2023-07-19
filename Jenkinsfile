node {
    stage('Take code from Git') { 
        git 'https://github.com/MariiaGalitsyna/jenkins_training.git'
    }
    stage('Results') {
        bat '''javac HelloWorld.java
               java HelloWorld'''
    }
    stage('Create archive') {
        bat "tar file: 'dnmgmttool.tar.gz'"
    }
}