#!/bin/
def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"

pipeline {
   agent any   
       stages {
	       stage ("compile") {
		    steps {
			    dir (project_path){
				    script{
					    if($buildchoice == "compile"){
						//bat 'mvn compile'
						build 'atmosphere-pipeline'
					    }
				    }
			    }
		     }
	       }
           	stage ("test") {
		    steps {
			  dir (project_path){
				  script{
					if($buildchoice == "test"){
					 bat 'mvn test'
					}
				  }
			  }
		     }
            	}
           	stage ("deploy") {
		    steps {
			dir (project_path){
				script{
					if($buildchoice == "deploy"){
					 bat 'mvn deploy'
					}
				}
			}
		     }
		}
	}   
}
