pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage ('check'){
            steps{
                git 'https://github.com/Minoo-YH/cal_3012_demo.git'
            }
        }
        stage ('build'){
            steps{
                bat 'mvn clean install'
            }
        }

        stage('test') {
            steps{
                bat 'mvn test'
            }
        }
        stage('jacoco'){
            steps{
                jacoco()
            }
        }
    }
}