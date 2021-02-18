pipeline {
    agent any
    stages {
        stage('SonarQube Analysis') {
            environment {
                scannerHome = tool 'SonarScanner'
            }
            steps {
                echo 'Preparing report...'
                withSonarQubeEnv('SonarServer') {
		  
                    sh "gradle sonarqube"
                }
            }
        }
	  
	      stage('Deployment') {
            steps {
		            echo 'Deployment stage....'
  	         }
	      }
    }
}
