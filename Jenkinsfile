pipeline {
    agent { label 'jenkins-Agent' }
    tools {
	jdk 'java17'
	maven 'Maven3'
    }
    stages{
	stage("Cleanup Workspace"){
		steps {
		cleanWs()
		}
	}
	    
	stage("Checkout from SCM"){
	        steps {
		git branch: 'main', credentialsId: 'github', url: 'https://github.com/muni77-sh/register-app'
	        }
	}
	    
       stage("Build Application"){
	       steps {
	       sh "mvn clean package"
	       }
        }
    }
}
