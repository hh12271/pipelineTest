pipeline {
	agent any
	tools {
    	maven 'local-maven'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git url: 'https://github.com/hh12271/pipelineTest.git'          	 
           	 
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
        stage("Package") {          	 
        	steps {  	 
            	sh "mvn package"          	 
       	    }
       	
        }
}
}
