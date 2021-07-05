pipeline{
    agent any
    environment {
        SERVER = 'dev'
    }
    parameters {
        string(name: 'VERSION', description: 'Please select the version that you want to deploy')
    }
    stages{
        stage('Build the code'){
            steps{
                sh 'mvn clean compile install'
            }
        }
        stage('Sending email'){
            steps
            {
                echo "This email is getting triggered from the $BUILD_NUMBER"
                echo "This email is getting triggered from the ${SERVER}"
            }            
        }        
    }
}    