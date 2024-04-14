pipeline {
  agent any
 tools{
	 maven 'maven3'
	 jdk 'jdk11'
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


