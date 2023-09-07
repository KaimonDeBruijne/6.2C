#!groovy
pipeline {
    agent any

    stages{
        stage('Build'){
            steps {
                echo "Compile and package the code with Gradle"
            }
        }
        stage ('Unit and Integration Tests') {
            steps {
                echo "Perform a Unit test: Test each module of the software using Katalon"
                echo "Perform an Integration test: Test all modules of the software using Katalon"
            }
        }
        stage ('Code Analysis') {
            steps {
                echo "Perform automated analysis of the code using SonarQube"
                echo "Pause for manual code analysis"
                sleep(10)
            }
        }
        stage ('Security Scan') {
            steps {
                echo "Scan the code for security vulnerabilities using AHS (Automated Security Helper)"
            }
        }
        stage ('Deploy to Staging') {
            steps {
                echo "Code deployed to AWS EC2 Staging Instance"
            }
        }
        stage ('Integration Test on Staging') {
            steps {
                echo "Perform an Integration test: Test all modules of the software using Katalon"
            }
        }
        stage ('Deploy to Production') {
            steps {
                echo "Code deployed to AWS EC2 Production Stage Instance"
            }
        }
    }
}
// test3