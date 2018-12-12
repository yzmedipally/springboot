pipeline {
   agent any   
       stages {
           stage ("one") {
                    steps {
                       echo "This is stage 1 print"
                    }
           }
           stage ("Two") {
                     steps {
                         input("Do you want me to continue")
                     }
            }
           stage ("Three") 
	   {
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

//def workspacesetup()
//{
//  def workspace = "learngit";
 // dir (workspace)
  
// }
