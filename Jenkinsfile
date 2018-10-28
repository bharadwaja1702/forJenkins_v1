node {
    stage('Example') {
        try {
            sh 'exit 1'
        }
        catch (exc) {
            echo 'Something failed, I should sound the klaxons!'
        }
    }
    stage('abc'){
        def a=10
        echo a
    }
}
