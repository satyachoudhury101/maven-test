pipeline {
 agent none
 stages{
  stage("build and SonarQube Analysis")
  {
   agent any
    steps {
	 withSonarQubeEnv('SonarQubeServer')
	 {
	  sh "mvn clean package sonar:sonar -Dsonar.projectKey=TokenSonarJenkinsProject1 -Dsonar.projectName='SonarJenkinsProject'"
	 }
	}
  }
 }
}
