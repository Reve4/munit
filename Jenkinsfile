pipeline
{
 agent any
 stages{
   stage('Build Application'){
   steps{
   bat 'mvn clean install -DskipTests'
   }
   }
   
 stage('Deploy Application'){
   steps{
   bat 'mvn package -DskipTests deploy -DmuleDeploy'
   }
   }
   
}
}
