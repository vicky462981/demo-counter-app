pipeline {
  agent any
 tools{
	maven 'M3'
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
		script{
	   withSonarQubeEnv(installationName:'sonarqubeserver',credentialsId:'Sonar_qube') {
		  sh 'mvn sonar:sonar -Dsonar.projectKey=your_project_key'

	   }
		}

	}
    
}
	}
			
	}




