node() {
    // agent { docker { image 'maven:3.9.3-eclipse-temurin-11' } }
    stage('build') {
        {
            bat 'set'
            bat 'echo Command executed'
        }
    }
    stage('Example') {
        if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
        } else {
            echo 'I execute elsewhere'
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
