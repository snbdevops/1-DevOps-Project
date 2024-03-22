@Library('my_jenkins_shared_libs') _

pipeline{
    agent any
    stages{
        stage('Git Checkout stage'){
            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/snbdevops/1-DevOps-Project.git"
                )
            }
        }
    }
}