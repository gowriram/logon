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

