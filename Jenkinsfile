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
}
}


