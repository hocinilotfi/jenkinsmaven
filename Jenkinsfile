pipeline{
    agent any 
    stages{
        stage('verifier maven'){
            steps{
                sh 'mvn -v'
            }
        }
        stage('clean et installer les dependance'){
            
            steps{
                 withMaven {
                    sh 'mvn clean'
                }
            }
        }
        stage('execution des tests'){
             
            steps{
                withMaven {
                sh 'mvn test'
            }
             }

        }
    }
    post{
        always{
            sh 'echo "affichage du rapport"'
        }
    }
}