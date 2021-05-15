pipeline {
	agent any
	tools {
    	maven 'Default'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
              git branch: 'main', url: 'https://github.com/gabbythomas/sample-spring-maven-app.git'          	 
        	}    
    	}
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
}
