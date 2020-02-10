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
                create_team_json(JSON)
                update_project_json(JSON)
               col_p_pr_det(JSON)
               fetch_teams_org(JSON)
               fetch_cntrl_org(JSON)
               fetch_build_settings(JSON)
               fetch_build_list(JSON)
               fetch_team()
             // delete_team()
             // delete_proj_json(JSON)
                }
            }
       
        
        
    }
}


