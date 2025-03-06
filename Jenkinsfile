pipeline {
 agent none
 stages{
  stage("build and SonarQube Analysis")
  {
   agent any
    steps {
	 withSonarQubeEnv('SonarQubeServer')
	 {
	  sh "mvn clean verify sonar:sonar \
  -Dsonar.projectKey=SonarJenkinsProject \
  -Dsonar.projectName='SonarJenkinsProject' \
  -Dsonar.host.url=http://34.100.145.62:9000 \
  -Dsonar.token=sqp_6bd2b5fc6b21e25c6974424c83047a4d2154a34d'"
	 }
	}
  }
 }
}
