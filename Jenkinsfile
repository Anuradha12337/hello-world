pipeline{
  agent any
  tools {
    maven 'maven3'
   }
   stages{
       
       stage('Maven build/Package'){
          steps{
               sh 'mvn clean package'
      }
    }

  }

}
