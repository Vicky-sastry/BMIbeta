@Library('shlib3')_
         pipeline{
    agent any

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
                  
    



