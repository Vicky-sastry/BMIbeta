@Library('shlib')_
         pipeline{
    agent any
    tools {
        maven "Maven"   
    }   
  /*  environment{
        sonarscanner = tool 'SonarScanner'
    }*/
    stages {
        stage('azureconnector')
        {
            steps
            {
                azureconn()
            }
        }
        stage('azurecollector')
        {
            steps
            {
                azurecol()
            }
        }
    }
         }
                  
    



