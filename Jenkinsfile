#!groovy​

pipeline {
    agent any
    stages {
        stage('Check File 0') {
            steps {
                echo fileExists ('file1').toString()
                echo "0: file1 checked"
            }
        }
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
                if (fileExists('file1')) {
                    echo 'Gibbet'
                } else {
                    echo 'Gibbet nischd'
                }
                //echo fileExists('file1').toString()
                echo "2: file1 checked"
            }
        }
    }
}
