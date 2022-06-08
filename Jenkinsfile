#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'python:3.10-slim'
            args '-u root'
        }
    }

    stages {
        stage('Initialize') {
            steps {
                echo 'Initializing...'
                sh '''python --version
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