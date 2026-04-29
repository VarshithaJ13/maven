pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch:'main',url:'https://github.com/VarshithaJ13/maven.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}