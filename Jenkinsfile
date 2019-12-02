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
echo "hello"
sh 'npm install' 
sh 'npm ls'
sh 'npm audit fix'
                       } 
     } 
     stage('S3-Deploy' ) 
     {
               steps{
echo "here" 
                       } 
     } 
        

    } 
}

