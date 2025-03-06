pipeline {
 agent none
 stages{
  stage("build and SonarQube Analysis")
  {
   agent any
    steps {
	 withSonarQubeEnv('SonarQubeServer')
	 {
	  sh "mvn clean package sonar:sonar -Dsonar.projectKey=jenkins-project1 -Dsonar.projectName='jenkins-project1'"
	 }
	}
  }
 }
}
