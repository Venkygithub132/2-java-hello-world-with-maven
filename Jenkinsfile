pipeline{
    agent any
    stages{
        stage("Build the code"){
            steps{
                sh mvn clean compile install
            }
        }
    }
}    