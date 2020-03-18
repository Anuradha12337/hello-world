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
<<<<<<< HEAD
             sh 'mvn clean package'
   }
  }
=======
         sh 'mvn clean package'
         
     }
   }

>>>>>>> bba4cca2713ab4f547cbb84d4df8c2e7f050b770
 }

}
