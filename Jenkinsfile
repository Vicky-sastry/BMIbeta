pipeline {
    libraries{
     lib 'shlib'
}
   agent any
    tools {
        maven "Maven"   
    }   
  
   stages {
       stage('Delete azure project')
       {
           steps{
               azpartproject()
           }
       }
               
       
      /*  stage('azureconnector')
        {
            steps
            {
                azureconn()
                logfun("is created")
            }
            post{
                failure{
                    logfun("is not created")
                }
            }
           
        }
        stage('azurecollector')
        {
            steps
            {
                azurecol()
                logfun2(" are listed")
            }
            post{
                failure{
                    logfun2("is not fetched")
                }
            }
        }*/
    }

}
