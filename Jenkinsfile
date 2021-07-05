pipeline{
    agent any
    environment {
        SERVER = "dev"
    }
    stages{
        stage('Build the code'){
            steps{
                sh 'mvn clean compile install'
            }
        }
        stage('Sending email'){
            steps{
                echo "This email is getting triggered from the $SERVER"
            }
            steps{
                echo "This email is getting triggered from the $BUILD_NUMBER"
            }            
        }        
    }
}    