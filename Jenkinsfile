pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            when{
               expression { return env.BRANCH_NAME == "origin/main" }
            }
            steps{
                bat "dotnet restore"
            }
        }
        stage("Build the project"){
             when{
               expression { return env.BRANCH_NAME == "origin/main" }
            }
            steps{
                bat "dotnet build"
            }
        }
        stage("Run tests"){
            when{
               expression { return env.BRANCH_NAME == "origin/main" }
            }
            steps{
                bat "dotnet test --no-build --verbosity normal"
            }
        }    
    }
}