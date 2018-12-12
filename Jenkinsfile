#!/bin/groovy

def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"

pipeline {
   agent any   
       stages {
	       stage ("one") {
		    steps {
			    dir (project_path){
  		        echo "This is stage 1 print"
			    }}
      		}
           	stage ("Two") {
                     steps {
                         input("Do you want me to continue")
                     }
            	}
           	stage ("Three") {
                        when {
                              not{ 
                                    branch "master"
                              }
                         }
                       steps {
                               echo "This is stage 3 print"
                       }
             	}
	}   
}

def workspacesetup(path)
{
  def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"
  dir (project_path)
}
