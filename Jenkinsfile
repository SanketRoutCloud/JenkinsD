pipeline {
    tools {
        jdk 'JAVA_HOME2'       // Ensure the tool name matches with what is configured in Jenkins Global Tool Configuration
        maven 'MAVEN_HOME2'     // Same here for Maven
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
