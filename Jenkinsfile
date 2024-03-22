@Library('my_jenkins_shared_libs') _

pipeline{
    agent any
    stages{
        stage('Step-1: Git Checkout stage'){
            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/snbdevops/1-DevOps-Project.git"
                )
            }
        }
        stage('Step-2: Unit Test Maven'){
            steps{
                script{
                    mvmTest()
                }
            }
        }
        stage('Step-3: Integration Test Maven'){
            steps{
                script{
                    mvnIntegrationTest()
                }
            }
        }        
    }
}