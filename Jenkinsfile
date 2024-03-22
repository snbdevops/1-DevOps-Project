@Library('my_jenkins_shared_libs') _

pipeline{
    agent any

    parameters{
        choice{name: 'action', choices: 'create\ndelete', description: 'Choose create/destroy'}
    }

    stages{

        stage('Step-1: Git Checkout stage'){

        when { expression {param.action == 'create' } }

            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/snbdevops/1-DevOps-Project.git"
                )
            }
        }
        stage('Step-2: Unit Test Maven'){

            when { expression {param.action == 'create' } }            

            steps{
                script{
                    mvmTest()
                }
            }
        }
        stage('Step-3: Integration Test Maven'){

            when { expression {param.action == 'create' } }   

            steps{
                script{
                    mvnIntegrationTest()
                }
            }
        }
        stage('Step-4: Static Code Analysis: Sonarqube'){

            when { expression {param.action == 'create' } }   

            steps{
                script{
                    statiCodeAnalysis()
                }
            }
        }                
    }
}