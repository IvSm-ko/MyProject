// Powered by Infostretch 

timestamps {

node () {

	stage ('GitApp - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a75c7a3e-4e70-482c-b0ef-1d11158ba4d3', url: 'https://github.com/IvSm-ko/MyProject.git']]]) 
	}
	stage ('GitApp - Build') {
 		// Maven build step
		withMaven(maven: 'mvn') { 
 			if(isUnix()) {
 				sh "mvn -f pom.xml clean test " 
			} 
			else { 
 				bat "mvn -f pom.xml clean test " 
			}	 
 		} 
	}
}
}
