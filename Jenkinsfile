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
echo "here" 
                       } 
     } 
        

    } 
}

