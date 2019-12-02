pipeline{

agent any
   stages
    {

       stage('Checkout-GIT') 
     {
               steps{
checkout scm
                       } 
     }
       stage('Node-Build') 
     {
               steps{
nodejs('Newnode') {
    // some block
sh 'npm install' 
sh 'npm ls'
sh 'npm audit fix'
} 
echo "hello"

                       } 
     } 
     stage('S3-Deploy' ) 
     {
               steps{
s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 's3-node1', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: true, selectedRegion: 'us-east-2', showDirectlyInBrowser: false, sourceFile: '*/', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 's3', userMetadata: []
                       } 
     } 
        

    } 
}

