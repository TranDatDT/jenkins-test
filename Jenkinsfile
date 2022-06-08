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
                sh 'python --version'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'pip install requests'
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