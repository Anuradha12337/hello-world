node{
    stage('SCM checkout'){
        
       git "https://github.com/Anuradha12337/hello-world"
     }
    stage('Compile-Package'){
      def mvnHome = tool name: 'maven3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
     }
    stage('Deploy to Tomcat'){
      sshagent(['tomcat-dev']){

      sh "scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.43.139"
     }
   }
 }
