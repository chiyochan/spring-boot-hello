pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                gradle clean build
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
