pipeline {
	agent any
	tools {
    		maven 'Default'
	}
	stages {
    		stage('Build') {
			steps {
				sh "mvn compile"  	 
          		}
    		}
    		stage("Unit test") {          	 
        		steps {  	 
              			sh "mvn test"          	 
       			}
      		}
   	}
	post {
		always {
			cleanWs()
		}
	}
}
