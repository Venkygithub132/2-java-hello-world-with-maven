pipeline{
    agent any
    environment {
        SERVER = 'dev'
    }
    parameters {
        choice(name: 'VERSION', choices: ['1.1', '1.2', '1.3'], description: 'select the version you want to deploy from drop down')
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
    post{
        always{
            echo "This step will be executed even if your build becomes success or fail"
        }
        success{
            echo "This step will be execued only if your build becomess success"
        }
        failure{
            echo "This step will be execued only if your build becomess failed"
        }
    }
}    