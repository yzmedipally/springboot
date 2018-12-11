pipeline {
    
	agent any
	
	environment {
        ENV_NAME = "${env.BRANCH_NAME}"
	echo ENV_NAME
    	}
	
		def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"
		dir(project_path)	
			stages {
				 	stage ("clean"){
						  bat 'mvn clean'
					}
					stage ("verify"){
						  bat 'mvn verify'
					} 
					stage ("compile"){
						  bat 'mvn compile'
					}
					stage ("package"){
						  bat 'mvn package'
					}
					stage ("Install"){
						  bat 'mvn install'
					}
					stage ("Artifact"){
						  archiveArtifacts "target/*.jar"
					}
				}
}
