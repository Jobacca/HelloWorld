#!groovy​

pipeline {
    agent any
    stages {
        stage('Create File') {
            steps {
                sh "touch file1"
                echo "file1 created"
            }
        }
        stage('Check File 1') {
            steps {
                if (fileExists('file1')) {
                    echo 'File exists'
                } else {
                    echo 'File doesn't exists'
                }
                echo "1: file1 checked"
            }
        }
        stage('Remove File') {
            steps {
                deleteDir()
                echo "file1 removed"
            }
        }
        stage('Check File 2') {
            steps {
                if (fileExists('file1')) {
                    echo 'File exists'
                } else {
                    echo 'File doesn't exists'
                }
                echo "2: file1 checked"
            }
        }
    }
}
