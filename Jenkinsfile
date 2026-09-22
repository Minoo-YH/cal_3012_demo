pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('check'){
            steps {
               git 'https://github.com/ADirin/cal_3012_demo.git'
            }
        }
        stage('build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('JaCoCo') {
            steps {
                jacoco()
            }
        }
    }
}