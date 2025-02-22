pipeline{
  tools{
    jdk 'JAVA_HOME2'
	maven 'M2_HOME2'
  }
  agent any
  stages{
   stage('checkout')
   {
     steps{
	   git 'https://github.com/SanketRoutCloud/JenkinsD.git'
	 }
   }
   stage('compile')
   {
     steps{
	   bat 'mvn compile'
	 }
   }
   stage('test')
   {
     steps{
	   bat 'mvn test'
	 }
   }
   stage('package')
   {
     steps{
	   bat 'mvn package'
	 }
   }
  }
}
