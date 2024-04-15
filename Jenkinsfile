pipeline {
  agent any
 tools{
	maven 'M3'
 }
	    environment {
        PATH = "/path/to/sonar-scanner/bin:$PATH"
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
		   echo 'Workspace Path: ${env.WORKSPACE}'

		   sh 'sonar-scanner -Dsonar.report.export.path=report-task.txt'
		  sh 'mvn sonar:sonar'

	   }
		}

	}
    
}
	}
			
	}




