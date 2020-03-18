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
    stage('Nexus Deploy'){
          steps{
            scripts{
            def pomfile = readMavenPom file: 'pom.xml'
            def version = pomfile.version
            def nexuRepo = version.endWith("SNAPSHOT") ? "pets-app-snapshot" : "pets-app-release"
            nexusArtifactUploader artifacts: [[artifactId: 'maven-project',
             classifier: '', file: '/var/lib/jenkins/workspace/Declarative_Pipeline_Job/webapp/target/webapp.war', 
             type: 'webapps.war']], credentialsId: 'nexus3', 
             groupId: 'com.example.maven-project', 
             nexusUrl: '172.31.13.164:8081', 
             nexusVersion: 'nexus3', protocol: 'http', 
             repository: 'nexusRepo', 
             version: '1.0-SNAPSHOT'
             version: version
           }
      }
    }

  }

}
