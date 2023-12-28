pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from GitHub
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/sainadhjaladi/pipeline.git']]])
            }
        }

        stage('Run') {
            steps {
                // Run your Java application
                bat 'javac Nothing.java' // Replace with your actual Java file name
                bat 'java Nothing'
            }
        }
    }
}
