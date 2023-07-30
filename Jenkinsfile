@Library('my-shared-library') _

pipeline{
    
    agent any

    /*parameters{
        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/destroy')
    }*/

    stages{

        stage('Git checkout'){

            //when { expression {  params.action == 'create' } }
            steps{

                

                    gitCheckout(
                        branch: "main",
                        url: "https://github.com/tenjomo/tenji-devops.git"
                    )

        }
        /*stage('Build'){

            when { expression {  params.action == 'create' } }
            steps{

                script{

                    mvnTest()
                }
            }

        }
        stage('Test'){

            when { expression {  params.action == 'create' } }
            steps{

                script{

                    mvnIntegrationTest()
                }
            }

        }
        stage('Static code analysis: Sonar'){

            when { expression {  params.action == 'create' } }
            steps{

                script{

                    def SonarQubecredentialsId = 'gene-token'
                    statiCodeAnalysis(SonarQubecredentialsId)
                }
            }

        }*/
    }
}
