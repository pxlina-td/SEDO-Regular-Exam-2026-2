pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            when{
                branch "main"
            }
            steps{
                bat "dotnet restore"
            }
        }
        stage("Build the project"){
             when{
                branch "main"
            }
            steps{
                bat "dotnet build"
            }
        }
        stage("Run tests"){
            when{
                branch "main"
            }
            steps{
                bat "dotnet test --no-build --verbosity normal"
            }
        }    
    }
}