pipeline{
  agent any
  tools{
   mavan3 'maven'
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
     }
   }

 }

}
