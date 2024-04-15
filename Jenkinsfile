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
	stage("static code nalysis"){
	steps{

     sh ''' $SCANNER_HOME/bin/sonar-scanner -Dsonar.url=http://13.233.173.216:9000/ -Dsonar.login=441c9d84efb64697125681a543b307c650d9beb9 -Dsonar.projectName=Myproject \
     -Dsonar.java.binaries=. \
     -Dsonar.projectKey=Myproject '''

	   }
		}

	}
    
}
	
			
	




