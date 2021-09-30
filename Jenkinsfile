pipeline
{
 agent any
 stages{
   stage('Build Application'){
   steps{
   bat 'mvn clean install -DskipTests'
   }
   }
   stage('Mail'){            
    steps{               
     echo "Ok"            
    }        
   } 
  stage('Check'){
   steps{     
   always {            
    emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'        
   }   
  }
  }
   
}
}
