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
               var=$(curl --location --request GET 'https://dev.azure.com/vickysastryvs/_apis/projects/mani?api-version=5.1' \
                     --header 'Accept: application/json' \
                     --header 'Authorization: Basic dmlja3lzYXN0cnkudnNAb3V0bG9vay5jb206enN4YXBrajN6d2s2cnR6N3ptNHR5bGk3YXlrN3l0NXllaHA1aWM3ZXJsZWM0eHNmN3R5YQ==') 
              echo $(var) 
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
