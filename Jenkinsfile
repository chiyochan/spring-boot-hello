#!groovy

pipeline {
    agent any


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
		sh 'gradle build'

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
