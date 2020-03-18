pipeline{
  agent any
  tools{
   name: 'maven3', type: 'maven'
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
