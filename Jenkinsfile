/* Requires the Docker Pipeline plugin */
pipeline {
    agent {
        node { label 'jkangent' }
          }
    
    stages {

      /*  stage ('Clone repository') {
            steps {
                checkout scm
            }
        }*/
        
        stage('build') {
            agent {
                docker {
                    image 'gradle:8.14.0-jdk21-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'gradle -g gradle-user-home --version'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing ...'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying ...'
            }
        }
    }
}
