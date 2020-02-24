pipeline {
    libraries{
     lib 'shlib'
}
   agent any
    tools {
        maven "Maven"   
    }          
    stages{
        /*stage('Hubot')
        {
            steps{
                examples()
            }
        }*/
        stage('User fetch'){
            steps{
                wrap([$class: 'BuildUser']) {
          sh 'echo "${BUILD_USER}"'
        }
            
            }
        
        }
        stage('All builds'){
            steps{
                
            sh "curl -X GET http://3.16.152.69:8080/job/jenkinsgame/api/json?tree=builds[number,status,timestamp,id,result] -u vicky:11f637872d1e4ad949af6ac3add0118812"
            }
        }
        
        
    //  stage('AZURE')
    //    {
        //    steps
       //     {
        
              //  fetchpushes(JSON)
                //fetchcommits(JSON)
              //  fetchpullrequests(JSON)
                //storeoutput(JSON)
                //influxpushazrepo()
          //  }
               /* create_project_json(JSON)
                log_function("Azure", "Project created")
                storeoutput(JSON)
                log_function("Azure", "Output stored")
                create_team_json(JSON)
                log_function("Azure", "Team created")
                update_project_json(JSON)
                 log_function("Azure", "Project Updated")
                col_p_pr_det(JSON)
                log_function("Azure", "Particular Project Details Fetched")
               fetch_teams_org(JSON)
                log_function("Azure", "Teams of an organisation Fetched")
               fetch_cntrl_org(JSON)
                log_function("Azure", "Controllers Fetched")
               fetch_build_settings(JSON)
                log_function("Azure", "Fetched Build Settings")
               fetch_build_list(JSON)
                log_function("Azure", "Fetched Build list")
               fetch_team()
                log_function("Azure", "Project Teams Fetched ")
             // delete_team()
              //  log_function("Azure", "Project Team Deleted ")
             // delete_proj_json(JSON)
                //log_function("Azure", "Project Deleted ")
            }*/

              
            
       
    }
}


