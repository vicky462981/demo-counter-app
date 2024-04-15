pipeline {
  agent any
 tools{
	maven 'M3'
 }
	environment{
	SCANNER_HOME=tool 'sonar-scanner'
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
	stage("static code nalysis"){
	steps{
	   withSonarQubeEnv('sonarqubeserver') {
		   sh ''' $scanner_HOME/bin/sonar-scanner -Dsonar.projectName=myprojt\
                  Dsonar.java.binaries=. \
		  .Dsonar.projectKey=myprojt
    		'''

	   }

	}
    
}
	}
			
	}




