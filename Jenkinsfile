pipeline
{
agent any
   stages
    {

         stage('Fetching-in-WorkSpace') 
        {
                 steps{
                        checkout scm
                       } 
        }
         stage('Node-Build') 
       {
               steps{
                      nodejs('Newnode') 
                     {
                      // dependies download
                         sh 'npm install' 
                         sh 'npm ls'
                         sh 'npm audit fix'
                         echo "nodejs build finish and issues resolved" 
                      } 
                     } 
       } 
       
        
    // stage('S3-Deploy' ) 
   //  {
   //            steps{
// s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 's3-node1', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: true, selectedRegion: 'us-east-2', showDirectlyInBrowser: false, sourceFile: '*/', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 's3', userMetadata: []
       //                } 
    // } 
        

    } 
}

