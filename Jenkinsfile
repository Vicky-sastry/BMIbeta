pipeline {
    libraries{
     lib 'shlib'
}
   agent any
    tools {
        maven "Maven"   
    }   
  
      /*stage('Delete azure project')
       {
           steps{
              /* var="$(curl --request GET 'https://dev.azure.com/vickysastryvs/_apis/projects/mani?api-version=5.1' \
                     --header 'Accept: application/json' \
                     --header 'Authorization: Basic dmlja3lzYXN0cnkudnNAb3V0bG9vay5jb206enN4YXBrajN6d2s2cnR6N3ptNHR5bGk3YXlrN3l0NXllaHA1aWM3ZXJsZWM0eHNmN3R5YQ==')" 
              */
              // curl https://dev.azure.com/vickysastryvs/_apis/projects/a48d59b2-f8a0-4ca5-a87f-5330921fa9fb -o output.json
              /* sh ''' 
               curl  --request GET 'https://dev.azure.com/vickysastryvs/_apis/projects/mani?api-version=5.1' \
                     --header 'Accept: application/json' \
                     --header 'Authorization: Basic dmlja3lzYXN0cnkudnNAb3V0bG9vay5jb206enN4YXBrajN6d2s2cnR6N3ptNHR5bGk3YXlrN3l0NXllaHA1aWM3ZXJsZWM0eHNmN3R5YQ==' -o output.json
               '''
           }
       }*/
               
    stages{
        
      stage('create project')
        {
            steps
            {
                create_project_json(JSON)
                storeoutput(JSON)
                
            }
        }
          stage('Update Project')
        {
            steps
            {
                update_project_json(JSON)
                
            }
        }
            stage('Team Creation')
            {
                steps{
                    create_team_json(JSON)
                }
            }
        
           
       stage('Fetch Particular project Details')
        {
            steps
            {
               col_p_pr_det(JSON)
                }
            }
        stage('Teams fetching')
            {
                steps{
                    fetch_teams_org(JSON)
                }
            }
         stage('Controllers fetching')
            {
                steps{
                    fetch_cntrl_org(JSON)
        }
    }
        stage('Build settings fetching')
            {
                steps{
                    fetch_build_settings(JSON)
        }
    }
        stage('Build list fetching')
            {
                steps{
                    fetch_build_list(JSON)
                }
            }
         stage('Deleting a project')
            {
                steps{
                    delete_proj_json(JSON)
                }
            }
        
    }
}


