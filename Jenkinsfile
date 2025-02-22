pipeline {
    tools {
        jdk 'JAVA_HOME2' // Make sure this matches the name of the JDK in your Jenkins Tool Configuration
        maven 'MAVEN_HOME2' // Ensure this is the correct Maven tool name
    }
    agent { label 'windows' }
    environment {
        JAVA_HOME = "C:\\Program Files\\Java\\jdk-17" // Explicitly set the JAVA_HOME variable
        PATH = "${JAVA_HOME}\\bin;${env.PATH}" // Add JAVA_HOME bin directory to PATH
    }
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
