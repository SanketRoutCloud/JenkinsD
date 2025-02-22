pipeline {
    tools {
        jdk 'JAVA_HOME2' 
        maven 'MAVEN_HOME2' 
    }
    agent { label 'windows' }
    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/SanketRoutCloud/JenkinsD.git'
            }
        }
        stage('compile') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
