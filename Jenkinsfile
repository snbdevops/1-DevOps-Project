pipeline{
    agent any
    stages{
        stage('Git Checkout stage'){
            steps{
                script{
                    git branch: 'main', url: 'https://github.com/snbdevops/1-DevOps-Project.git'
               }
            }
        }
    }
}