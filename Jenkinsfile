pipeline {
    agent any
    environment { 
        CC = 'clang'
    }    
    stages {
        stage('Build') {
            steps {
                
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'first', passwordVariable: 'abcdefg', usernameVariable: 'bharath'), usernamePassword(credentialsId: 'first', passwordVariable: 'abcdefg', usernameVariable: 'bharath1')]) {
    // some block
                      echo 'Testing..'
            } 
            }
  parallel linux: {
    node('linux') {
        checkout scm
        try {
            unstash 'app'
            sh 'make check'
        }
        finally {
            junit '**/target/*.xml'
        }
    }
  },
   windows: {
    node('windows') {
        /* .. snip .. */
    }
 }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
         stage('Example') {
            steps {
               // mail to bharadwaj.ambati@itpeoplecorp.com, subject: 'The Pipeline failed :('
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
         stage('Example1') {
            environment { 
                DEBUG_FLAGS = '-g'
            }
            steps {
                echo env.DEBUG_FLAGS
            }
        }
        
    }  
    
    
}
