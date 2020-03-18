pipeline{
  agent any
  tools {
    maven 'maven3'
   }
  
  stages{
    stage('SCM checkout'){
       steps{
       git "https://github.com/Anuradha12337/hello-world"
     }
  
  }
  stage('Maven build/Package'){
       steps{
         sh 'mvn clean package'
         tool name: 'maven3', type: 'maven'
     }
   }

 }

}
