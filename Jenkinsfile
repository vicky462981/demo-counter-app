pipeline {
  agent any

stages{
	stage('git clone'){
	steps{
		git branch: 'main', url: 'https://github.com/vicky462981/demo-counter-app'
		
		
	}
	stage("build"){
	steps{
		mvn clean insrall
	}
	}
}
}
