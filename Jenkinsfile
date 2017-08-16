#!groovy​

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                pwd()
                echo "build finished"
            }
        }
        stage('Test') {
            steps {
                echo "test finished"
            }
        }
        stage('Deploy') {
            steps {
                echo "test finished"
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
