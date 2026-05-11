pipeline {

    agent any

    tools {
        maven 'maven3'
        jdk 'JDK17'
    }

    stages {

        stage('Checkout') {

            steps {

                git branch: 'main',
                    url: 'https://github.com/YOUR_USERNAME/maven-ci-cd-demo.git'
            }
        }

        stage('Build') {

            steps {

                sh 'mvn clean compile'
            }
        }

        stage('Test') {

            steps {

                sh 'mvn test'
            }
        }

        stage('Package') {

            steps {

                sh 'mvn package'
            }
        }
    }
}
