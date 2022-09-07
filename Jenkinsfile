pipeline{
    agent any
    stages{
        stage("Maven Build"){
            when {
                branch "develop"
            }
            steps{
                sh "mvn package"
            }
        }
        stage("Deploy to dev"){
            when {
                branch "develop"
            }
            steps{
                echo "deploy to development server...."
            }
        }
        stage("Deploy To production"){
            when {
                branch "master"
            }
            steps{
                echo "deploy to master server...."
            }
        }
    }
}
      
