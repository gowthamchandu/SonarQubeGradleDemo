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
		    sh "chmod +x gradlew"
                    sh "./gradlew sonarqube"
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
