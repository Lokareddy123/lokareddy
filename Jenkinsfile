@Library("hellolibs") _
pipeline{
    agent any
    stages{
        stage("Git Checkout"){
            steps{
                git credentialsId: 'github', url: 'https://github.com/Lokareddy123/lokareddy.git'
            }    
            
        }
        stage("Maven Build"){
            steps{
                sh 'mvn clean package'
            }    
        }
        stage("Dev Tomcat Deploy"){
            steps{
                tomcatDeploy("172.31.81.20","ec2-user","tomcat-dev")
            }    
        }
    }
}  
  
  
      
