pipeline {
  agent any
 tools{
	 maven 'Maven 3.9.6'
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


