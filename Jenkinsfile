pipeline{
  agent any
  tools{
   mavan 'maven3'
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
