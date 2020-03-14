node{
    stage('SCM checkout'){
        
     git "https://github.com/Anuradha12337/hello-world"
     }
    stage('Compile-Package'){
      def mvnHome = tool name: 'maven3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
     }
   }
