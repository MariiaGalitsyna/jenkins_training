node {
    stage('Example') {
        if (env.BRANCH_NAME == 'test') {
            echo 'I only execute on the test branch'
        } else {
            echo 'I execute elsewhere'
        }
    }
    stage('More steps'){
        set
        echo  'Command executed'
    }
}

   