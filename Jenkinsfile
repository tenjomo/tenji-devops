@Library('my-shared-library') _

pipeline{
    
    agent any

    parameters{
        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/destroy')
    }

    stages{

        stage('Git checkout'){

            when { expression {  params.action == 'create' } }
            steps{

                script{

                    gitCheckout(
                        branch: "main",
                        url: "https://github.com/tenjomo/tenji-devops.git"
                    )
                }
            }

        }
        stage('Unit test maven'){

            when { expression {  params.action == 'create' } }
            steps{

                script{

                    mvnTest()
                }
            }

        }
        stage('Integration test maven'){

            when { expression {  params.action == 'create' } }
            steps{

                script{

                    mvnIntegrationTest()
                }
            }

        }
    }
}