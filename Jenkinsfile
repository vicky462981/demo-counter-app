pipeline {
  agent any
  tools{
	jdk 'jdk-11'
	maven 'maven'
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


