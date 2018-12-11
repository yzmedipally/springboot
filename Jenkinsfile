
pipeline {
    
	agent any
	
	stages {
		
		dir('/spring-boot-samples/spring-boot-sample-atmosphere'){	

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
}
