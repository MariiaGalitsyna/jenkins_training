node {
    stage('Example') {
        if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
        } else {
            echo 'I execute elsewhere'
        }
    }
    stage('More steps'){
        bat 'set'
        bat 'echo Command executed'
    }
}

   