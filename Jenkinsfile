#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'python:3.10-slim'
        }
    }

    stages {
        stage('Initialize') {
            steps {
                echo 'Initializing...'
                sh '''python --version
                whoami
                '''
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'pip install requests --user --no-cache'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'python main.py'
            }
        }
    }
}