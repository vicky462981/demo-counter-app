pipeline {
  agent any
 tools{
	maven 'M3'
 }
environment{
	SCANNER_HOME= tool 'sonarscannner'
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
	
			
	




