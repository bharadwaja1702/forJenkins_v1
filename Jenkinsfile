pipeline {
    agent any
    environment { 
        CC = 'clang'
    }    
    stages {
        stage('Build1') {
            steps {
                
                echo 'Building..'
            }
        }
        stage('Test1') {
            /* parallel linux: {
              node('linux') {
                 checkout scm
                 try {
                        unstash 'app'
                       sh 'make check'
                   }
                      finally {
                    junit '**///target/*.xml'
               /*  }
             }
            },
              windows: {
               node('windows') {
                  
               }
            }*/
            steps {
                echo 'Testing....'
            }
        }
        
        stage('Deploy1') {
            steps {
                echo 'Deploying....'
                }
        }
         stage('Example1') {
            steps {
               // mail to bharadwaj.ambati@itpeoplecorp.com, subject: 'The Pipeline failed :('
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
    
    
}
