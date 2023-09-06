#!groovy
pipeline {
    agent any

    environment {
        DIRECTORY_PATH= "projects/5.1P"
        TESTING_ENVIRONMENT= "5.1P_TEST"
        PRODUCTION_ENVIRONMENT= "KAIMON DE BRUIJNE"
    }
    
    stages{
        stage('Build'){
            steps {
                echo "Fetch the source code from $DIRECTORY_PATH"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage ('Test') {
            steps {
                echo "Unit tests"
                echo "Integration test"
            }
        }
        stage ('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage ('Deploy') {
            steps {
                echo "Deploy the application to $TESTING_ENVIRONMENT"
            }
        }
        stage ('Approval') {
            steps {
                sleep(10)
            }
        }
        stage ('Deploy to Production') {
            steps {
                echo "Code deployed to $PRODUCTION_ENVIRONMENT production environment"
            }
        }
    }
}