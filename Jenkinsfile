pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                echo "Build"
                sh 'gradle clean build'
            }

        }

        stage ('Test') {
            steps {
                echo "Test"
            }

        }

        stage ('Deploy') {
            steps {
                echo "Deploy"
            }

        }


    }
    }
