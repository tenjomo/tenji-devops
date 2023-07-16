pipeline{
    
    agent any

    stages{

        stage('Git checkout'){

            steps{

                script{

                    git branch: 'main', url: 'https://github.com/tenjomo/tenji-devops.git'
                }
            }

        }
    }
}