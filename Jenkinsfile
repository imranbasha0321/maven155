@Library('sharedlibrary')_
pipeline
{
    agent any
    stages
    {
        stage('contDownload')
        {
            steps
            {
            script
            {
                cicd.gitDownload("maven")
            }
        }
    }
     stage('contbuild')
     {
         steps 
         {
             script
             {
                 cicd.buildmaven()
             }
         }
     }
     stage('contDeployment')
     {
         steps
         {
          script
          {
              cicd.tomcatdeploy("declarativepipelinewithsharedlibrary","172.31.21.68","mytestapp")
          }   
         }
     }
     stage('contTesting') 
     {
         steps 
         {
             script
             {
                 cicd.gitDownload("FunctionalTesting")
                 cicd.runselinium("declarativepipelinewithsharedlibrary")
                 
             }
         }
     }
    
}
}


