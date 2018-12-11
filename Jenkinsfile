pipeline {
    
	agent any
	
	 environment {
		 LOCAL_BUILD_PATH="{env.WORKSPACE+'/spring-boot-samples/spring-boot-sample-atmosphere'}"
		 echo LOCAL_BUILD_PATH
        }
	
		dir(LOCAL_BUILD_PATH)	
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
