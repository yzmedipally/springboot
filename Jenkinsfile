#!/bin/
def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"

pipeline {
   agent any   
       stages {
	       stage ("compile") {
		    steps {
			    dir (project_path){
				    script{
					    if($Buildchoice == "compile"){
						bat 'mvn compile'
					    }
				    }}
		     }
	       }
           	stage ("test") {
		    steps {
			  dir (project_path){
				if($Buildchoice == "compile"){
				 bat 'mvn compile'
				}
			  }
		     }
            	}
           	stage ("deploy") {
		    steps {
			dir (project_path){
				if($Buildchoice == "compile"){
				 bat 'mvn compile'
				}
			}
		     }
		}
	}   
}
