pipeline{
    agent any 
    stages{
        stage('verifier maven'){
            steps{
                sh 'mvn -v'
            }
        }
        stage('clean et installer les dependance'){
             withMaven {
            steps{
                sh 'mvn clean install'
            }
            }
        }
        stage('execution des tests'){
             withMaven {
            steps{
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