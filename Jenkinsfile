#!groovy​

pipeline {
    agent any
    stages {
        stage('Create File') {
            steps {
                pwd()
                sh "touch file1"
                echo "file1 created"
            }
        }
        stage('Check File 1') {
            steps {
                echo fileExists ('file1').toString()
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
                echo fileExists('file1')
                echo "2: file1 checked"
            }
        }
    }
}
