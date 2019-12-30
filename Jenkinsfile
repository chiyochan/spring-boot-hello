pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                gradlew("clean" , "build")
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
