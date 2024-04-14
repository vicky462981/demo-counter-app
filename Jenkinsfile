pipeline {
  agent any
 tools{
	 maven 'MAVEN_HOME'
	 jdk11 'JAVA_HOME'
 }

stages{
	stage("git clone"){
	steps{
		git branch: 'main', url: 'https://github.com/vicky462981/demo-counter-app'	
		
	}
	}
	stage("Build"){
	steps{
		sh 'mvn clean install'
			
	}
	}
}
}


