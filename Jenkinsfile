pipeline {
    agent any
    environment { 
        CC = 'clang'
    }    
    stages {
        stage('Build') {
            steps {
                def prompt = {
  JFrame jframe = new JFrame()
  String answer = JOptionPane.showInputDialog(jframe, it)
  jframe.dispose()
  echo answer
}
                echo 'Building..'
            }
        }
        stage('Test') {
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
