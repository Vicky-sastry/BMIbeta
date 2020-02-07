pipeline {
    libraries{
     lib 'shlib'
}
   agent any
    tools {
        maven "Maven"   
    }          
    stages{
        
      stage('create project')
        {
            steps
            {
                create_project_json(JSON)
                storeoutput(JSON)
               // logfun("is created")   
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
        
        /*   
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
        stage('fetch teams of project')
        {
            steps{
                fetch_team()
            }
        }
        /* stage('Deleting a project')
            {
                steps{
                    delete_proj_json(JSON)
                }
            }
        */
        
        
    }
}


