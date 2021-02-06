pipeline {
	agent any
	tools {
    	maven 'my_mvn'
	}
	stages {
    	stage("Checkout") {
        	steps {
        	    git branch: 'master',
                url: 'git@github.com:CDSBeef/MavenTestPro.git'
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
