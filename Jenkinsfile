pipeline {
  agent any
  stages {
    stage('Build1') {
      steps {
        echo 'Building..'
      }
    }
    stage('Test1') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Testing....'
          }
        }
        stage('1') {
          steps {
            mail(subject: 'hey', body: 'sample jenkins mail', from: 'bharadwaj.ambati@itpeoplecorp.com', to: 'bharadwaj.ambati@itpeoplecorp.com')
          }
        }
        stage('2') {
          steps {
            echo 'mail send'
          }
        }
        stage('3') {
          steps {
            sh 'echo \'done\''
          }
        }
      }
    }
    stage('Deploy1') {
      steps {
        echo 'Deploying....'
      }
    }
    stage('Example1') {
      steps {
        echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
      }
    }
    stage('Example11') {
      environment {
        DEBUG_FLAGS = '-g'
      }
      steps {
        echo env.DEBUG_FLAGS
      }
    }
  }
  environment {
    CC = 'clang'
  }
}