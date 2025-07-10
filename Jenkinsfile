/* Requires the Docker Pipeline plugin */
pipeline {
    agent {
        node { label 'jkangent' }
          }
    stages {
        stage('build') {
            steps {
                sh 'docker version'
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
