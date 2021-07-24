#!groovy
@Library('standard') _

pipeline {
    agent any

    parameters {


    }

    stages {

        stage ('Checkout') {
            steps {
	    echo "Check out code"		    
	    git branch: 'dev', credentialsId: 'github-credentials', url: 'https://github.com/chiyochan/spring-boot-hello'	
            }

        }

        stage ('Build') {
            steps {
                echo "Build"

            }

        }

        stage ('Test') {
            steps {
                echo "Test"
                // bat 'gradle test'
            }

        }

        stage ('Deploy') {
            steps {
                echo "Deploy"			

            }

        }


    }
    }
