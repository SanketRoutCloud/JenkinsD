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
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
