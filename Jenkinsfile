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
                sh 'mvn clean install'
            }
        }
        stage('execution des tests'){
            steps{
                sh 'mvn test'
            }
        }
    }
    post{
        always{
            sh 'echo "affichage du rapport"'
        }
    }
}