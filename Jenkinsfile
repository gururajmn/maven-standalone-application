pipeline {
    agent any

    parameters {
        string(name: 'STAGE_NAME', defaultValue: 'Build', description: 'Enter the stage name to execute')
    }

    stages {
        stage('Checkout') {
            when {
                expression { params.STAGE_NAME == 'Checkout' }
            }
            steps {
                echo 'Checking out the source code...'
                git branch: 'main', url: 'https://github.com/gururajmn/maven-web-application.git'
            }
        }

        stage('Build') {
            when {
                expression { params.STAGE_NAME == 'Build' }
            }
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            when {
                expression { params.STAGE_NAME == 'Test' }
            }
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            when {
                expression { params.STAGE_NAME == 'Deploy' }
            }
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}

